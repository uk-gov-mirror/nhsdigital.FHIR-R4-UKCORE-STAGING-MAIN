## {{page-title}}

<table class="assets">
<tr>
<th colspan="2">Context of Issue</th>
</tr>
<tr>
<td width="30%">Context: </td>
<td><a href="https://simplifier.net/hl7fhirukcorer4/ukcore-observation-averagebloodpressure" target="_blank">UKCore-Observation-AverageBloodPressure</a> (Profile), <a href="https://simplifier.net/hl7fhirukcorer4/valueset-ukcore-bloodpressure-average" target="_blank">UKCore-BloodPressure-Average</a> (ValueSet)</td>
</tr>
<tr>
<td width="30%">Type: </td>
<td>Profile, ValueSet</td>
</tr>
<tr>
<td width="30%">Source: </td>
<td>UK Core User Community</td>
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
Require clarification of the word 'average' to mitigate clinical risk. 
The existence of the profile UKCore-Observation-AverageBloodPressure
with its wording mentioning 'average' in unclear and creates a potential
clinical risk. There is also a lack of 'parameters'.
</td>
<td>
<b>Initial Proposal:</b>
<br /><br />
Need to understand a need for this profile as average has a variation of
meaning e.g. 24 hours, 72 hours, 30 days readings etc. Due to the uncertain
meaning of average, it is felt clinically to be unsafe to keep this resource.
If a resource is required, then keep generic Blood Pressure and then add
parameters e.g.: invasive blood pressure, laterality, position etc:
By doing this, the ValueSet is more constrained as the VS as-is is too large.
Until there is a use case and a requirement, this resource is too risky to
pursue as is.
<br /><br />
<b>Main Points Raised in C&TA Calls:</b>
<br /><br />
Kevin Sprague:
<ul>
<li>If no implementations depend on it, deprecate now; revisit when use case is clear.</li>
</ul>
Ann Wrightson:
<ul>
<li>Ask for direct, clear proposal sentence (“Retire the resource”) at the top, with rationale below.</li>
</ul>
</td>
</tr>
</table>