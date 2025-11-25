## {{page-title}}

<table class="assets">
<tr>
<th colspan="2">Context of Issue</th>
</tr>
<tr>
<td width="30%">Context: </td>
<td>sct-descid</td>
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
Use of sct-descId for mapping and READ codes. The extension is only for showing a non-preferred term within SCT, linking it with the preferred term. If using other codes systems and mapping to SCT then both would go in seperate .coding elements, with userSelected chosen to represent the original.
</td>
<td>
<b>Initial Proposal:</b>
<br /><br />
Remove the word 'SHALL' in the guidance.
Guidance <a href ="https://simplifier.net/guide/uk-core-implementation-guide-stu3-sequence/Home/Guidance/CodeableConcept-Guidance?version=0.10.0#Sending-a-SNOMED-CT-Description-ID-that-is-not-the-preferred-term" target="_blank">here</a><br /><br />
Remove the extension from this example as not part of explanation and can cause confusion.
Guidance <a href="https://simplifier.net/guide/uk-core-implementation-guide-stu3-sequence/Home/Guidance/CodeableConcept-Guidance?version=0.10.0#Rules-for-populating-legacy-coding" target="_blank">here</a>
<br /><br />
<b>Main Points Raised in C&TA Calls:</b>
<br /><br />
Ryan May:
<ul>
<li>Confirmed: Read code should be its own coding entry; don’t use the SCT descriptionId extension to carry non SNOMED codes; simplify example.</li>
</ul>
</td>
</tr>
</table>