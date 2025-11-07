---
subject: https://fhir.hl7.org.uk/StructureDefinition/Extension-UKCore-AllergyIntoleranceEnd
---


{{page:ExtensionTemplate}}

<div id="Examples" class="tabcontent">
  <h3>Examples</h3>
  <b>Allergy Intolerance End</b>- An example to illustrate the date when the allergy or intolerance was no longer valid, and/or, the reason why the allergy or intolerance is no longer valid.<br>
  {{pagelink:Extension-UKCore-AllergyIntolEnd-Example}}
  <br><br>
</div>

<h3 id="guidance-allergyintoleranceend">Extension Specific Guidance</h3>

An optional extension to record the date and reason when the allergy was no longer clinically `active`.<br/>
If the `AllergyIntolerance.clinicalStatus` is `active` then this extension SHALL be omitted.<br/>
If the `AllergyIntolerance.clinicalStatus` is `inactive` or `resolved` then the date and reason when the allergy was identified as no longer `active` SHOULD be populated.

---
