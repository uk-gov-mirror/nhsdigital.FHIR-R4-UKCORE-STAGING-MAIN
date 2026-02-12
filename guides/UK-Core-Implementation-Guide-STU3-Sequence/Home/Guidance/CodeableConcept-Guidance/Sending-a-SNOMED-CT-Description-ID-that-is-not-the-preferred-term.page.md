## Sending a SNOMED CT Description ID that is not the preferred term

In this case, the SNOMED CT Description ID represents a term that is different from the preferred term and therefore the description display will be different from that used to populate the <code>code.coding.display</code> element. Therefore the extension {{pagelink:Extension-UKCore-CodingSCTDescDisplay}} MAY be populated with the term corresponding to the selected SNOMED CT Description ID, as per the example below.

<div class="tab">
 <button class="tablinks active" onclick="openTab(event, 'table-view')">Table View</button>
 <button class="tablinks" onclick="openTab(event, 'tree-view')">Tree View</button>
 <button class="tablinks" onclick="openTab(event, 'xml-view')">XML View</button>
 <button class="tablinks" onclick="openTab(event, 'json-view')">JSON View</button>
</div>

<div id="table-view" class="tabcontent" style="display:block">
  <h3>Table View</h3>
{{table:Extension-UKCore-CodingSCT-Heart-Example}}
</div>

<div id="tree-view" class="tabcontent">
  <h3>Tree View</h3>
{{tree:Extension-UKCore-CodingSCT-Heart-Example, expand:9}}
</div>

<div id="xml-view" class="tabcontent">
  <h3>XML View</h3>
{{xml:Extension-UKCore-CodingSCT-Heart-Example}}
</div>

<div id="json-view" class="tabcontent">
  <h3>JSON View</h3>
{{json:Extension-UKCore-CodingSCT-Heart-Example}}
</div>

---
