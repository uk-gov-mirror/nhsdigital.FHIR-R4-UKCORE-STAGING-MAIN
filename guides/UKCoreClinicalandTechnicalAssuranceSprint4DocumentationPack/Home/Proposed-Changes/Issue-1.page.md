## {{page-title}}

<table class="assets">
<tr>
<th colspan="2">Context of Issue</th>
</tr>
<tr>
<td width="30%">Context: </td>
<td><a href="https://simplifier.net/HL7FHIRUKCoreR4/UKCore-Observation-Group-Lab" target="_blank">UKCore-Observation-Group-Lab</a> (Profile)</td>
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
<td>Proposed In Scope - Development Done</td>
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
Profile has become redundant due to new element (Observation.organizer) in R6.
</td>
<td>
<b>Initial Proposal:</b>
<br /><br />
<ul>
<li>Retire UKCore-Observation-Group-Lab.</li>
<li>Create guidance on using the new backport.</li>
<li>Amend existing Group-Lab examples to use backport.</li>
</ul>
<br />
<b>Main Points Raised in C&TA Calls:</b>
<br /><br />
Philip Brennan:
<ul>
<li>Confirms active work uses Observation + hasMember (EU pattern); this topic aligns with earlier grouping need.</li>
<li>Not uniform globally (some use DiagnosticReport as grouper), but majority trending to Observation hasMember; debate ongoing.</li>
</ul>
Ryan May:
<ul>
<li>Clarified distinction: earlier “grouping guidance” was generic; this item specifically retires the lab grouper.</li>
</ul>
Ian McNicoll:
<ul>
<li>Asked whether international consensus is forming on panel modelling.</li>
</ul>
</td>
</tr>
</table>