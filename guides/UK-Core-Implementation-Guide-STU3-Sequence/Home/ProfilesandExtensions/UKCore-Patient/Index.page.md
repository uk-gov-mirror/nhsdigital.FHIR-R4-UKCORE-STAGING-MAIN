---
topic: UKCore-Patient
subject: https://fhir.hl7.org.uk/StructureDefinition/UKCore-Patient
usage: http://hl7.org/fhir/StructureDefinition/Patient
---

<nospellcheck>

{{page:ProfileTemplate_new}}

</nospellcheck>


<div id="ProfileGuidance">

### Example Usage Scenarios ###

The following are example usage scenarios for the UK Core Patient profile:

- Query for Patient demographic information using the query parameter `Patient.identifier` for a known NHS number.
- Query for Patient demographic information using query parameters such as `Patient.name.family`, `Patient.name.given`, `Patient.birthDate`, and `Patient.gender`.
- Exchange Patient demographic information within a FHIR document or message.

<hr class="thickline">

## Profile Specific Implementation Guidance: ##

{{page:ProfileMustSupportTemplate}}

</div>

---
