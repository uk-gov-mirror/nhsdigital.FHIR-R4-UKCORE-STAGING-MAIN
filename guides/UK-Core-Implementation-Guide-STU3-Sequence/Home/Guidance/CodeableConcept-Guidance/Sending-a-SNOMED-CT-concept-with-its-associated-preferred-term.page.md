## Sending a SNOMED CT concept with its associated preferred term 

When sending a SNOMED CT Concept Id with its preferred term, and the SNOMED CT Description Id is known, then the HL7 core-defined extension <a href="https://hl7.org/fhir/R4/extension-coding-sctdescid.html" class="external">coding-sctdescid</a> SHALL be used and the element `sctdescid` SHALL be populated. Where the SNOMED CT Description Id is not known, then the codeable concept MAY be sent without it.

In the example below, the SNOMED CT Description Id is populated with the Id of the preferred term, but there is no display term, as the Concept Id was entered by the user and the preferred term was displayed to them when it was added.

<div class="tab">
  <button class="tablinks active" onclick="openTab(event, 'table-view')">Table View</button>
 <button class="tablinks" onclick="openTab(event, 'tree-view')">Tree View</button>
  <button class="tablinks" onclick="openTab(event, 'xml-view')">XML View</button>
  <button class="tablinks" onclick="openTab(event, 'json-view')">JSON View</button>
  <button class="tablinks feedback" onclick="openTab(event, 'Feedback')">Feedback</button>

</div>

<div id="table-view" class="tabcontent" style="display:block">
  <h3>Table View</h3>
{{table:Extension-UKCore-CodingSCT-Myocardial-Example}}
</div>

<div id="tree-view" class="tabcontent">
  <h3>Tree View</h3>
{{tree:Extension-UKCore-CodingSCT-Myocardial-Example, expand:9}}
</div>

<div id="xml-view" class="tabcontent">
  <h3>XML View</h3>
{{xml:Extension-UKCore-CodingSCT-Myocardial-Example}}
</div>

<div id="json-view" class="tabcontent">
  <h3>JSON View</h3>
{{json:Extension-UKCore-CodingSCT-Myocardial-Example}}
</div>
<div id="Feedback" class="tabcontent">
  <h3>Feedback</h3>
Click here to: {{page:FeedbackLink}}</a>
</div>

---