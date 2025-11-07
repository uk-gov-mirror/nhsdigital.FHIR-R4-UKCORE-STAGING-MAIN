## {{page-title}}

<table class="assets">
<tr>
<th colspan="2">Context of Issue</th>
</tr>
<tr>
<td width="30%">Context: </td>
<td><a href="https://simplifier.net/hl7fhirukcorer4/ukcore-observation-tobaccoconsumption" target="_blank">UKCore-Observation-TobaccoConsumption</a> (Profile), <a href="https://simplifier.net/hl7fhirukcorer4/valueset-ukcore-tobaccoconsumption" target="_blank">UKCore-TobaccoConsumption</a> (ValueSet)</td>
</tr>
<tr>
<td width="30%">Type: </td>
<td>Modelling</td>
</tr>
<tr>
<td width="30%">Source: </td>
<td>UK Core Development Team</td>
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
tobaccoConsuption profile only allows valueQuantity, but SNOMED CT UK has codes such as 160603005 &verbar; Light cigarette smoker (1-9 cigs/day) (finding)&verbar;
</td>
<td>
<b>Initial Proposal:</b>
<br /><br />
Propose loosening up to allow valueCodeableConcepts, with a valueset to include all types of tobacco use.
<br /><br />
<b>Main Points Raised in C&TA Calls:</b>
<br /><br />
Ann Wrightson:
<ul>
<li>Revisit purpose and usage contexts (what needs comparability?); minimise UX burden.</li>
</ul>
Sian Musto:
<ul>
<li>If quantities are captured, categories can be derived—understand why categorical terms are needed vs raw measures.</li>
</ul>
Andrew Perry:
<ul>
<li>Origin may be PRSB; will analyse GP usage stats for pre coordinated smoking concepts; note QoF complexity and that status ≠ single recording.</li>
</ul>
Ian McNicoll:
<ul>
<li>Clinical priority is smoking status (current/ex/never) as the key risk factor; allowing coded consumption is fine, but ensure status is addressed (e.g., separate profile/element).</li>
</ul>
Kanthan Theivendran:
<ul>
<li>Points to openEHR Tobacco Smoking Summary as a good reference for clinical data elements; AU FHIR uses archetypes to guide shapes.</li>
</ul>
Charlie McCay:
<ul>
<li>Primary fix now: correct the value set description (it wrongly says “level of consciousness”).</li>
<li>Don’t over generalise—keep this profile focused on consumption; create separate value sets/profiles for smoking status and other perspectives; document intended use and misuse explicitly.</li>
</ul>
Kevin Sprague:
<ul>
<li>Agreed: update description; consider additional artefacts but avoid burdening implementers.</li>
</ul>
</td>
</tr>
</table>