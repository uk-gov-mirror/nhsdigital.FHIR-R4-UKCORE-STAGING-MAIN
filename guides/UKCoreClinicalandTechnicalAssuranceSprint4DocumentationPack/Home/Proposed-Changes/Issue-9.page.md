## {{page-title}}

<table class="assets">
<tr>
<th colspan="2">Context of Issue</th>
</tr>
<tr>
<td width="30%">Context: </td>
<td><a href="https://simplifier.net/hl7fhirukcorer4/extension-ukcore-codingsctdescdisplay" target="_blank">Extension-UKCore-CodingSCTDescDisplay</a> (Extension)</td>
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
<td>Confirmed In Scope</td>
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
The IG guidance states that if the sct-descId is sent, then the UK Core sctdescDisplay SHALL be used.
</td>
<td>
<b>Initial Proposal:</b>
<br /><br />
The requirement should be changed from SHALL to MAY.

Click <a href="https://simplifier.net/guide/UK-Core-Implementation-Guide-STU3-Sequence/Home/Guidance/CodeableConcept-Guidance?version=current#Sending-a-SNOMED-CT-Description-ID-that-is-not-the-preferred-term" target="_blank">here</a>
<br /><br />
<b>Main Points Raised in C&TA Calls:</b>
<br /><br />
Kevin Sprague:
<ul>
<li>There’s a live vendor issue suggesting UK Core diverges from base FHIR behavior; reviewing; may need options (including deprecation).</li>
</ul>
Ann Wrightson:
<ul>
<li>While under review, relaxing to MAY helps implementers and reduces harm.</li>
</ul>
Charlie McCay:
<ul>
<li>This should be solved internationally (HL7 + SNOMED), not by a UK only extension; avoid extending extensions; basic FHIR–SNOMED integration must be straightforward.</li>
</ul>
Ryan May:
<ul>
<li>Context: the need was to send a non preferred term text alongside the conceptId; past misuse included sending descriptionIds as codes.</li>
</ul>
</td>
</tr>
</table>