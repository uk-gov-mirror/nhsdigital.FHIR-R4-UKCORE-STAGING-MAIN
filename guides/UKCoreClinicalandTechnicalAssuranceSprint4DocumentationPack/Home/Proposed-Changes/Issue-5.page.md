## {{page-title}}

<table class="assets">
<tr>
<th colspan="2">Context of Issue</th>
</tr>
<tr>
<td width="30%">Context: </td>
<td>All FHIR assets</td>
</tr>
<tr>
<td width="30%">Type: </td>
<td>FHIR asset lifecycle process</td>
</tr>
<tr>
<td width="30%">Source: </td>
<td>UK Core Developement Team</td>
</tr>
<tr>
<td width="30%">Scope: </td>
<td>Confirmed In Scope - Development Done</td>
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
Having 'active' status after C&TA causes confusion due to:
<ul>
<li>once active, cannot go back to draft, can only change to retired</li>
<li>changes may be breaking, but goes against active status as may still be worked on before ballot</li>
<li>many draft assets not being worked on and no use case</li>
</ul>
</td>
<td>
<b>Initial Proposal:</b>
<br /><br />
Proposals:

draft - actively worked on ready for ballot. Will show in build only
active - balloted
retired - not to be used for future work, but needs to be available for historical use. Does this need to be in a package?

Click <a href="https://simplifier.net/guide/UK-Core-Implementation-Guide-STU3-Sequence/Home/Guidance/Lifecycle?version=current" target="_blank">here</a> for more information.
<br /><br />
<b>Main Points Raised in C&TA Calls:</b>
<br /><br />
Kevin Sprague:
<ul>
<li>Historically made Active after Clinical & Technical Assurance (vendors reluctant to implement Draft).</li>
<li>Proposal now: Active only after ballot; pre ballot content remains Draft but marked “assured” if it has been.</li>
<li>Needs careful back shuffling and explanation in next release.</li>
</ul>
Ben McAlister:
<ul>
<li>Wants clear distinguishability between balloted and non balloted content.</li>
</ul>
Ann Wrightson:
<ul>
<li>This belongs in the broader process refresh; current profile status options constrain what we can do; ensure consultation/engagement continues in any new model.</li>
</ul>
Ryan May:
<ul>
<li>HL7 UK working group will address this; must get it right the first time.</li>
</ul>
</td>
</tr>
</table>