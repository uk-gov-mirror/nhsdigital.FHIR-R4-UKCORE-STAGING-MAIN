---
topic: Library-Extensions-PreAdopt
---
## Cross Version Extensions

Elements from other FHIR versions can be used within R4 by applying the relevant cross‑version extension packages. This enables implementers to incorporate newer elements without fully upgrading to a newer FHIR release.

Links for the R5 elements to R4 can be found at https://hl7.org/fhir/uv/xver-r5.r4/0.1.0/ 

See <a href="https://confluence.hl7.org/spaces/FHIRI/pages/413256623/FAQs">HL7 Confluence: Cross Version Extensions FAQs</a> for more details

### R6 Cross-version extensions

A cross version extension package is expected to be released when R6 has become normative. Until then extensions will have to be created manually. Below is a list that have been created. Note: these extensions will be removed once the new xver-r6.r4 extension package has been released.

<fql>
from StructureDefinition
where
    type = 'Extension' 
    and status != 'retired'
    and url.contains('http://hl7.org/fhir/')
select
    'Id': id, 'Context of Use':context.expression, 'url': url,'Status':status
</fql>


<script>
$(document).ready(function () {
    const queryString = window.location.search || "?version={{guide-version}}";
    
    // Detect if we are in a preview/unpublished guide by checking if .page.md is in the URL
    const isUnpublished = window.location.search.includes("version=current");

    const extensionBase = "https://simplifier.net/guide/uk-core-implementation-guide-stu3-sequence/home/profilesandextensions/extensionlibrary/";
    const profileBase = "https://simplifier.net/guide/UK-Core-Implementation-Guide-STU3-Sequence/Home/ProfilesandExtensions/UKCore-";

    const extSuffix = isUnpublished ? ".page.md" : ""; // only use .page.md in preview

    const $table = $("table.table-bordered");
    if ($table.length === 0) return;

    $table.find("tbody tr").each(function () {
        const $cells = $(this).find("td");
        if ($cells.length < 2) return;

        const $extensionCell = $cells.eq(0);
        const $profilesCell = $cells.eq(1);

        // --- Extension Column ---
        const extText = $extensionCell.text().trim();
        if (extText) {
            const extHref = `${extensionBase}${extText}${extSuffix}${queryString}`;
            $extensionCell.html(`<a href="${extHref}">${extText}</a>`);
        }

        // --- Profiles Column ---
        const profilesRaw = $profilesCell.text().trim().split(";");
        const profileLinks = profilesRaw.map(profile => {
            const clean = profile.trim();
            if (!clean) return "";

            if (clean === "Coding") return "Coding";

            const resource = clean.split(".")[0];
            const profileHref = `${profileBase}${resource}${queryString}`;
            return `<a href="${profileHref}">${clean}</a>`;
        }).filter(link => link);

        $profilesCell.html(profileLinks.join("<br>"));
    });
});
</script>



---