## {{page-title}}

<table class="assets">
<tr>
<th colspan="2">Context of Issue</th>
</tr>
<tr>
<td width="30%">Context: </td>
<td><a href="https://simplifier.net/hl7fhirukcorer4/ukcore-encounter" target="_blank">Encounter</a> (Profile), <a href="https://simplifier.net/hl7fhirukcorer4/ukcore-appointment" target="_blank">Appointment</a> (Profile), <a href="https://simplifier.net/hl7fhirukcorer4/ukcore-slot" target="_blank">Slot</a> (Profile)</td>
</tr>
<tr>
<td width="30%">Type: </td>
<td>Binding</td>
</tr>
<tr>
<td width="30%">Source: </td>
<td><a href="https://simplifier.net/hl7fhirukcorer4/ukcore-appointment/~issues/3273" target="_blank">Simplifier Issue</a></td>
</tr>
<tr>
<td width="30%">Scope: </td>
<td>Proposed In Scope</td>
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
Appointment/Slot binds to http://terminology.hl7.org/CodeSystem/service-type
</td>
<td>
<b>Initial Proposal:</b>
<br /><br />
Propose to bind to https://fhir.hl7.org.uk/ValueSet/UKCore-CareSettingType
(Uses SNOMED CT UK Refset with fully specified name 'Services simple reference set’) as it does in Encounter
<br /><br />
<b>Main Points Raised in C&TA Calls:</b>
<br /><br />
Kevin Sprague:
<ul>
<li>Binding strength likely preferred (advisory, not enforced); this improves guidance without mandating.</li>
</ul>
</td>
</tr>
</table>