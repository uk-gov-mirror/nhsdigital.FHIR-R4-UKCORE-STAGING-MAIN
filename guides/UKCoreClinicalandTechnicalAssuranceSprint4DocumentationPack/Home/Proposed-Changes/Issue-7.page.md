## {{page-title}}

<table class="assets">
<tr>
<th colspan="2">Context of Issue</th>
</tr>
<tr>
<td width="30%">Context: </td>
<td>Sex</td>
</tr>
<tr>
<td width="30%">Type: </td>
<td>Implementation Guide</td>
</tr>
<tr>
<td width="30%">Source: </td>
<td>UK Core Development Team</td>
</tr>
<tr>
<td width="30%">Scope: </td>
<td>Proposed Out of Scope</td>
</tr>
</table>
<br>
<table class="assets">
<tr>
<th width="50%">Issue</th>
<th width="50%">Proposal</th>
</tr>
<tr>
<td>
There are many different extensions representing the sex of a patient, as well as Patient.gender. There is no clear guidance on which extensions, or the Patient.gender element, should be used for which use case.
</td>
<td>
<b>Initial Proposal:</b>
<br /><br />
There are many different extensions for sex:
<ul>
<li>Patient.gender</li>
<li>https://build.fhir.org/ig/HL7/fhir-extensions/StructureDefinition-individual-recordedSexOrGender.html</li>
<li>https://build.fhir.org/ig/HL7/fhir-extensions/StructureDefinition-patient-sexParameterForClinicalUse.html</li>
<li>https://build.fhir.org/ig/HL7/fhir-extensions/StructureDefinition-individual-genderIdentity.html
https://simplifier.net/hl7fhirukcorer4/extension-ukcore-birthsex</li>
</ul>
<br />
<b>Main Points Raised in C&TA Calls:</b>
<br /><br />
No main points raised.
</td>
</tr>
</table>