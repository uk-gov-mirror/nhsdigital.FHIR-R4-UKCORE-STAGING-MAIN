---
topic: UKCore-Observation-VitalSigns
subject: https://fhir.hl7.org.uk/StructureDefinition/UKCore-Observation-VitalSigns
usage: http://hl7.org/fhir/StructureDefinition/Observation
---


<nospellcheck>

{{page:ProfileTemplate_new}}

</nospellcheck>


<div id="ProfileGuidance">

### Example Usage Scenarios ###

The following are example usage scenarios for the UK Core Observation Vital Signs profile:

- Query and retrieve a patient's vital signs
- Record or update a patient's vital signs

<hr class="thickline">

## Profile Specific Implementation Guidance: ##

This is a derived profile of {{pagelink:UKCore-Observation,text:UKCore-Observation}} and this page only shows the differences between the two. Refer to the base Profile for more implementation guidance.

This guidance is also designed to align with [https://hl7.org/fhir/R4/observation-vitalsigns.html](HL7 Observation Vital Signs guidance) where possible.

The guidance on this page also applies to the following profiles, that are derived from the UK Core Observation Vital Signs profile:
- {{pagelink:UKCore-Observation-VitalSigns-BloodPressure}}
- {{pagelink:UKCore-Observation-VitalSigns-BMI}}
- {{pagelink:UKCore-Observation-VitalSigns-BodyHeight}}
- {{pagelink:UKCore-Observation-VitalSigns-BodyTemperature}}
- {{pagelink:UKCore-Observation-VitalSigns-BodyWeight}}
- {{pagelink:UKCore-Observation-VitalSigns-HeadCircumference}}
- {{pagelink:UKCore-Observation-VitalSigns-HeartRate}}
- {{pagelink:UKCore-Observation-VitalSigns-OxygenSaturation}}
- {{pagelink:UKCore-Observation-VitalSigns-RespirationRate}}

### Mandatory and Must Support Data Elements

The following elements, in addition to those in the corresponding {{pagelink:UKCore-Observation,text:UKCore-Observation}} parent profile, are identified as MustSupport, and it is expected that consumers and suppliers SHALL support these as per the {{pagelink:Guidance-MustSupport}}.

<table class="assets" title="MustSupport element list">
<tr>
<th class="width30">Element</th>
<th class="width70">Reason</th>
</tr>
<tr>
<td><code>Observation.status</code></td>
<td>A status of <code>final</code> SHALL be present.</td>
</tr>
<tr>
<td><code>Observation.category</code></td>
<td>A category of <code>vital-signs</code> SHALL be present.</td>
</tr>
<tr>
<td><code>Observation.code.coding</code></td>
<td>A LOINC "magic code" SHALL be present, in addition to the SNOMED CT concept for the observation type.</td>
</tr>
<tr>
<td><code>Observation.subject</code></td>
<td>A UKCore-Patient SHALL be present.</td>
</tr>
<tr>
<td><code>Observation.effective[x]</code></td>
<td>An effective time or date SHALL be present.</td>
</tr>
<tr>
<td><code>Observation.component.code.coding</code></td>
<td>If a component is present, a LOINC "magic code" SHALL be present, in addition to the SNOMED CT concept for the observation type.</td>
</tr>
</table>
</div>

---

