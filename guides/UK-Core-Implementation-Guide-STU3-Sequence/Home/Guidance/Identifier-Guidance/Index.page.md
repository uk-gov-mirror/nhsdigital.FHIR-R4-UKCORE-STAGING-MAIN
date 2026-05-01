# {{page-title}}

<div id="newAsset" markdown="span" class="alert alert-success" role="alert"><h4><i class="fa fa-star"></i></h4>
<h2> Principles</h2>
The following principles apply to the definition and use of identifier systems within UK Core–conformant implementations:


- Uniqueness is the primary requirement for an identifier system, although excessive specialisation reduces long‑term usefulness and semantic value.


- Identifier systems SHOULD NOT carry meaning. Consumers SHOULD NOT derive semantics from the structure or contents of the system or value. Identifier systems exist solely to establish uniqueness and scope.

- Ownership of identifiers SHOULD be clear.
Ideally, the system generating the identifier is represented by a unique identifier system URI. Where this is not possible, the organisation that owns and manages the identifiers should be considered the authority for that system.


- Identifier system URIs MAY change over time.
Implementations SHOULD NOT assume system URIs are permanently resolvable or immutable. Most healthcare data has a limited operational lifespan, and identifier systems may evolve accordingly.


- Use of the NamingSystem resource is OPTIONAL.
NamingSystem resources are intended for historical reference and documentation only. 


- Do not rely on assigner or type for processing or search.
Best practice is to avoid dependence on Identifier.assigner or Identifier.type, as neither element is reliably searchable across implementations.

See <a href="https://build.fhir.org/datatypes.html#Identifier">DataTypes - Identifier</a> and <a href="https://build.fhir.org/ig/HL7/fhir-for-fair/FHIRidentifiers.html">FHIR for FAIR - FHIR Identifiers</a>for more information

<h2>Identifier System Example Approach</h2>

Where a recognised identifier system exists, or one can reasonably be established:

Systems SHOULD use the published identifier system as the default.
The system URI SHALL uniquely identify the namespace in which identifier values are issued.

Vendor‑Defined Identifier Systems
Where no nationally or regionally defined identifier system exists:

Suppliers MAY define their own identifier system using a vendor‑controlled URI.
The URI DOES NOT NEED to be resolvable, but SHALL be globally unique.
Responsibility for uniqueness and lifecycle management rests with the defining vendor.

Organisational Fallback Pattern
If neither a standard nor vendor‑defined system is available, the following organisational pattern MAY be used:

```json
identifier: [
    {
    system: <org-id-system>/<org-code>/<specialism>,
    value: <local-id>
    }
]
``` 


Example

```json
identifier: [
    {
    system: https://fhir.nhs.uk/Id/ods-site-code/1234/pathology-specimenvalue,
    value: R1234
    }
]
``` 


The system URI defines the organisational and functional scope.
The value is unique only within that system.
Consumers MUST NOT interpret meaning from either the system path or the identifier value.
</div>
