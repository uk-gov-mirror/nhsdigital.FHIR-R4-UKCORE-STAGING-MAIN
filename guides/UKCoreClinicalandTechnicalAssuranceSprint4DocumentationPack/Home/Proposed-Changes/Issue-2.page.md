## {{page-title}}

<table class="assets">
<tr>
<th colspan="2">Context of Issue</th>
</tr>
<tr>
<td width="30%">Context: </td>
<td><a href="https://simplifier.net/hl7fhirukcorer4/ukcore-observation-vitalsigns" target="_blank">UKCore-Observation-VitalSigns</a> (Profile)</td>
</tr>
<tr>
<td width="30%">Type: </td>
<td>Profiles</td>
</tr>
<tr>
<td width="30%">Source: </td>
<td>UK Core Developement Team</td>
</tr>
<tr>
<td width="30%">Scope: </td>
<td>Confirmed Out of Scope</td>
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
UKCore-VitalSigns has been derived from HL7 VitalSigns. This means we have to use LOINC codes, however:
<ul>
<li>all other vitalsigns not derived from hl7 specific vitalsigns, but from UKCore-VitalSigns, e.g. bmi, bp</li>
<li>blood pressure, not derived from http://hl7.org/fhir/bp.html. slicing different to hl7 defined bp profile</li>
<li>BodyWeight Internation uses unit = kg (required) , we use "kilogram". US seem to have made LOINC optional</li>
<li>bmi base definition incorrect, should be http://hl7.org/fhir/StructureDefinition/bmi</li></ul></td>
<td>
<b>Initial Proposal:</b>
<br /><br />
Review why we derived from HL7 base Observation-VitalSigns.

Options are:
<ul>
<li>Keep to HL7 derived Observation, even if against dm+d (e.g. no `m` in height valueset)</li>
<li>Derive from UK Core Observation and ignore HL7 derived Observation. This is possible as we are not deriving from them</li>
<li>Derive from UK Core but ensure closely aligned, where practicable, to HL7 profiles</li>
</ul>
<br />
<b>Main Points Raised in C&TA Calls:</b>
<br /><br />
Kevin Sprague:<br />
<ul>
<li>Agreed: “too big/complex” for a technical sprint; risk of breaking things.</li>
<li>Position this for a roadmap rather than quick fix.</li>
</ul>
<br />
Charlie McCay:<br />
<ul>
<li>Asked for explicit rationale in the pack for why issues are out of scope (not just a list).</li>
<li>Suggested also tracking proposed HL7 International changes arising from UK findings.</li>
</ul>

</td>
</tr>
</table>