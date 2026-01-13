## {{page-title}}

<table class="assets">
<tr>
<th colspan="2">Context of Issue</th>
</tr>
<tr>
<td width="30%">Context: </td>
<td><a href="https://simplifier.net/hl7fhirukcorer4/ukcore-observation-vitalsigns-bloodpressure" target="_blank">UKCore-Observation-VitalSigns-BloodPressure</a> (Profile)</td>
</tr>
<tr>
<td width="30%">Type: </td>
<td>Terminology Concepts</td>
</tr>
<tr>
<td width="30%">Source: </td>
<td><a href="https://simplifier.net/hl7fhirukcorer4/ukcore-observation-vitalsigns-bloodpressure/~issues/3297" target="_blank">Simplifer Issue</a></td>
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
There are 3 SNOMED CT codes used in this model top level to record the type of BP - then 2 codes to record the systolic and diastolic results/values.
</td>
<td>
<b>Initial Proposal:</b>
<br /><br />
For each top code it needs to be validated that there are clinically validated systolic concepts defined. Or even if the concept of systolic and diastolic is valid for CVP and invasive blood pressures. This need work with an expert in intensive care to validate.
<br /><br />
<b>Main Points Raised in C&TA Calls:</b>
<br /><br />
Ian McNicoll:
<ul>
<li>Keep the top level “BP” code generic (as a grouper); actual semantics live in systolic/diastolic children; trim the top level value set.</li>
</ul>
Ann Wrightson:
<ul>
<li>Document intended use as vital signs (ward/GP) to avoid scope creep.</li>
</ul>
Kevin Sprague:
<ul>
<li>Treat 17 & 18 together; align with existing work (Ian’s).</li>
</ul>
</td>
</tr>
</table>