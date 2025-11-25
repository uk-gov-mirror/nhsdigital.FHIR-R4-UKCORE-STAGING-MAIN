## {{page-title}}

<table class="assets">
<tr>
<th colspan="2">Context of Issue</th>
</tr>
<tr>
<td width="30%">Context: </td>
<td><a href="https://simplifier.net/hl7fhirukcorer4/valueset-ukcore-bloodpressure-systolic" target="_blank">UKCore-BloodPressure-Systolic</a> (ValueSet)</td>
</tr>
<tr>
<td width="30%">Type: </td>
<td>Terminology Concepts</td>
</tr>
<tr>
<td width="30%">Source: </td>
<td><a href="https://simplifier.net/hl7fhirukcorer4/valueset-ukcore-bloodpressure-systolic/~issues/3296" target="_blank">Simplifier Issue</a></td>
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
Concepts to use when recording central venous pressure.
Currently if you are representing a CVP or other invasive blood pressures,
which appear to be in scope, there are no appropriate concepts to record
the systolic and diasolic pressures. It would not be correct to use
271649006 &verbar; Systolic blood pressure (observable entity) as this is not
what it is. So to represent correctly you would need to use a concept
specifically for invasive blood pressure.
</td>
<td>
<b>Initial Proposal:</b>
<br /><br />
Propose to use a concept such as
276776003 &verbar;Right atrial pressure - a wave (observable entity) &verbar; or 276772001 &verbar;Right ventricular systolic pressure (observable entity)&verbar;.
This would need validating with clinical experts.
<br /><br />
<b>Main Points Raised in C&TA Calls:</b>
<br /><br />
Kevin Sprague:
<ul>
<li>Short term: disallow non systemic/invasive usages under this profile until clarified; align with prior work.</li>
</ul>
Ian McNicoll:
<ul>
<li>Distinguish systemic arterial blood pressure (vital signs) versus localised pressures (e.g., right atrial/ventricular).</li>
<li>Invasive is OK if it reflects systemic arterial BP; otherwise use different concepts.</li>
<li>Trim value sets; can share text/guidance and align with prior archetype work.</li>
</ul>
Ann Wrightson:
<ul>
<li>Clarify what is “not OK”: don’t use the generic BP profile for localised pressures; use appropriate alternative model.</li>
</ul>
Andrew Perry:
<ul>
<li>Support: restrict BP profiles to left sided/systemic meanings; document how to record alternatives.</li>
<li>Reminded that GP systems store triples (grouper + systolic + diastolic).</li>
</ul>
Kanthan Theivendran:
<ul>
<li>Clinically: ward/GP “BP” ≠ ICU pressures; e.g., RAP reflects diastolic—mismatch under current systolic value set.</li>
</ul>
</td>
</tr>
</table>