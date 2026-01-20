<fql>
from
	ValueSet
where
    status !='retired'
select
	ValueSet: id, Status: status, CodeSystem: compose.include.system, ValueSets: compose.include.valueSet
order by
	id
distinct
</fql>

<script>
$(document).ready(function () {
    const queryString = window.location.search || "?version=current";
    const isUnpublished = window.location.search.includes("version=current");
    const pageSuffix = isUnpublished ? ".page.md" : "";

    // Convert {{guide-title}} into URL-safe form
    const guideTitleUrl = "{{guide-title}}"
        .replace(/[^a-zA-Z0-9 ]/g, "")
        .replace(/\s+/g, "-");

    const baseUrl = `https://simplifier.net/guide/${guideTitleUrl}/Home/`;
    const vsBase = `${baseUrl}terminology/valuesets/valueset-`;
    const csBase = `${baseUrl}terminology/codesystems/codesystem-`;

    // Target the specific table rendered by FQL
    const $table = $("table.table-bordered");
    if ($table.length === 0) return;

    // 1. Fix Headers
    const $headerCells = $table.find("thead tr th");
    if ($headerCells.length >= 4) {
        $headerCells.eq(2).text("Composed of");
        $headerCells.eq(3).hide(); // Hide the redundant 4th column
    }

    // 2. Process Rows
    $table.find("tbody tr").each(function () {
        const $cells = $(this).find("td");
        if ($cells.length < 4) return;

        const $nameTd = $cells.eq(0);
        const $statusTd = $cells.eq(1);
        const $systemTd = $cells.eq(2);
        const $valueSetTd = $cells.eq(3);

        // --- Linkify the ValueSet Name (Column 1) ---
        const nameText = $nameTd.text().trim();
        if (nameText.toLowerCase().includes("ukcore")) {
            const assetLower = nameText.toLowerCase();
            const href = `${vsBase}${assetLower}${pageSuffix}${queryString}`;
            $nameTd.html(`<a href="${href}">${nameText}</a>`);
        }

        // --- Handle the "Composed of" logic (Columns 3 and 4) ---
        let combinedLinks = [];

        // Helper to extract URLs from comma-separated text in cells
        const extractAndLink = ($td) => {
            const rawText = $td.text().trim();
            if (!rawText) return;

            // SPLIT BY COMMA is the fix for Simplifier FQL output
            rawText.split(",").forEach(item => {
                const trimmed = item.trim();
                if (!trimmed) return;

                let href = trimmed;
                let displayText = trimmed;

                // Check if it's a UK Core URL that needs internal mapping
                if (trimmed.includes("fhir.hl7.org.uk")) {
                    const parts = trimmed.split("/");
                    const assetType = parts[3] ? parts[3].toLowerCase() : "";
                    const assetName = parts[4] ? parts[4].toLowerCase() : "";

                    if (assetType === "codesystem") {
                        href = `${csBase}${assetName.toLowerCase()}${pageSuffix}${queryString}`;
                    } else if (assetType === "valueset") {
                        href = `${vsBase}${assetName.toLowerCase()}${pageSuffix}${queryString}`;
                    }
                }
                
                combinedLinks.push(`<a href="${href}">${displayText}</a>`);
            });
        };

        extractAndLink($systemTd);
        extractAndLink($valueSetTd);

        // Remove duplicates and join with line breaks
        const uniqueLinks = [...new Set(combinedLinks)];
        
        $systemTd.html(uniqueLinks.join("<br>"));
        $valueSetTd.hide(); // Hide the extra column we merged
    });
});
</script>