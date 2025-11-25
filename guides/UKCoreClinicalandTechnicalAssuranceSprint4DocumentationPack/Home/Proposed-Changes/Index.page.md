## {{page-title}}

This section documents proposed changes to be applied to the UK Core for the next release. These are highlighted to allow reviewers to comment on the proposed changes. Solutions for the issues which lead to these proposed changes may have been discussed on the Clinical and Technical Assurance Sprint 8 calls but can still be challenged by any reviewer.

<table class="assets">
<tr>
<th width="8%">Number</th>
<th width="17%">Context</th>
<th width="9%">Type</th>
<th width="4%">Source</th>
<!--<th width="31%">Issue</th>
<th width="31%">Proposal</th>-->
<th width="21%">Issue</th>
<th width="20%">Proposal</th>
<th width="20%">Scope</th>
</tr>
<tr>
<td>{{pagelink:Issue-1}}</td>
<td><a href="https://simplifier.net/HL7FHIRUKCoreR4/UKCore-Observation-Group-Lab" target="_blank">UKCore-Observation-Group-Lab</a> (Profile)</td>
<td>Profiles</td>
<td>UK Core Developement Team</td>
<td>Profile has become redundant due to new element (Observation.organizer) in R6.</td>
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
<td>Proposed In Scope - Development Done</td>
</tr>
<tr>
<td>{{pagelink:Issue-2}}</td>
<td><a href="https://simplifier.net/hl7fhirukcorer4/ukcore-observation-vitalsigns" target="_blank">UKCore-Observation-VitalSigns</a> (Profile)</td>
<td>Profiles</td>
<td>UK Core Development Team</td>
<td>UKCore-VitalSigns has been derived from HL7 VitalSigns. This means we have to use LOINC codes, however:
<ul>
<li>all other vitalsigns not derived from hl7 specific vitalsigns, but from UKCore-VitalSigns, e.g. bmi, bp</li>
<li>blood pressure, not derived from http://hl7.org/fhir/bp.html. slicing different to hl7 defined bp profile</li>
<li>BodyWeight Internation uses unit = kg (required) , we use "kilogram". US seem to have made LOINC optional</li>
<li>bmi base definition incorrect, should be http://hl7.org/fhir/StructureDefinition/bmi</li></ul></td>
<td>
<b>Initial Proposal:</b>
<br /><br />
Review why the Profile is derived from HL7 base Observation-VitalSigns. Consider potential options.
Options are:
<ul>
<li>Keep to HL7 derived Observation, even if against dm+d (e.g. no `m` in height valueset)</li>
<li>Derive from UK Core Observation and ignore HL7 derived Observation. This is possible as we are not deriving from them</li>
<li>Derive from UK Core but ensure closely aligned, where practicable, to HL7 profiles</li>
</ul>
<br />
<b>Main Points Raised in C&TA Calls:</b>
<br /><br />
Kevin Sprague:<br />
<ul>
<li>Agreed: “too big/complex” for a technical sprint; risk of breaking things.</li>
<li>Position this for a roadmap rather than quick fix.</li>
</ul>
<br />
Charlie McCay:<br />
<ul>
<li>Asked for explicit rationale in the pack for why issues are out of scope (not just a list).</li>
<li>Suggested also tracking proposed HL7 International changes arising from UK findings.</li>
</ul>
</td>
<td>Proposed Out of Scope</td>
</tr>
<tr>
<td>{{pagelink:Issue-3}}</td>
<td>Profiles derived from Observation</td>
<td>Implementation Guide</td>
<td>UK Core Development Team</td>
<td>The predecessor to the UK Core C&TA7 was an NHSD Observations IG.
This gave much more information on how to use the Observations,
search terms, how they link. Now they are between all other Profiles
with not enough guidance on usage, as found with the PDM team.</td>
<td>
<b>Initial Proposal:</b>
<br /><br />
Propose splitting into separate IG to keep together with more specific
information on how to use.
<br /><br />
<b>Main Points Raised in C&TA Calls:</b>
<br /><br />
Kevin Sprague:
<ul>
<li>Process is currently disjointed (gap between tech assurance vs ballot); align road map first.</li>
<li>Acknowledged process hiccup; next Sprint should clarify inclusion/exclusion and sequencing.</li>
</ul>
Ben McAlister:
<ul>
<li>Observed derived profiles appear as active in the guide, causing confusion if they’re out of scope.</li>
</ul>
Ryan May:
<ul>
<li>Clarified the ballot status was draft, not balloted (corrected himself).</li>
</ul>
</td>
<td>Proposed Out of Scope</td>
</tr>
<tr>
<td>{{pagelink:Issue-4}}</td>
<td>Packages</td>
<td>Naming convention</td>
<td>UK Core Development Team</td>
<td>Each STU version of package has a different name.</td>
<td>
<b>Initial Proposal:</b>
<br /><br />
Propose using fhir.r4.ukcore x.0.0 to ensure standard approach and use correct project to separate major versions.
<br /><br />
<b>Main Points Raised in C&TA Calls:</b>
<br /><br />
Kevin Sprague:
<ul>
<li>It’s a process change reversing prior agreement; needs broader governance (HL7 UK / FIRE Board).</li>
</ul>
</td>
<td>Proposed Out of Scope</td>
</tr>
<tr>
<td>{{pagelink:Issue-5}}</td>
<td>All FHIR assets</td>
<td>FHIR asset lifecycle process</td>
<td>UK Core Development Team</td>
<td>Having 'active' status after C&TA causes confusion.</td>
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
<td>Proposed In Scope - Development Done</td>
</tr>
<tr>
<td>{{pagelink:Issue-6}}</td>
<td><a href="https://simplifier.net/hl7fhirukcorer4/ukcore-observation-averagebloodpressure" target="_blank">UKCore-Observation-AverageBloodPressure</a> (Profile), <a href="https://simplifier.net/hl7fhirukcorer4/valueset-ukcore-bloodpressure-average" target="_blank">UKCore-BloodPressure-Average</a> (ValueSet)</td>
<td>Profile, ValueSet</td>
<td>UK Core User Community</td>
<td>Require clarification of the word 'average' to mitigate clinical risk. 
The existence of the profile UKCore-Observation-AverageBloodPressure
with its wording mentioning 'average' in unclear and creates a potential
clinical risk. There is also a lack of 'parameters'.</td>
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
<td>Proposed In Scope</td>
</tr>
<tr>
<td>{{pagelink:Issue-7}}</td>
<td>Sex</td>
<td>Implementation Guide</td>
<td>UK Core Development Team</td>
<td>There are many different extensions representing the sex of a patient, as well as Patient.gender. There is no clear guidance on which extensions, or the Patient.gender element, should be used for which use case.</td>
<td>
<b>Initial Proposal:</b>
<br /><br />
Propose discussing how and where the patient's sex is described.
<br /><br />
<b>Main Points Raised in C&TA Calls:</b>
<br /><br />
No main points raised.
</td>
<td>Proposed Out of Scope</td>
</tr>
<tr>
<td>{{pagelink:Issue-8}}</td>
<td>Observation panel (group)</td>
<td>Implementation Guide</td>
<td>UK Core Development Team</td>
<td>Lack of clarity on how Observations should be grouped, with the most
common having unrelated items within a single Observation instance.</td>
<td>
<b>Initial Proposal:</b>
<br /><br />
Propose guidance around how to group observations, similar to the lab one. May include creating an Observation-Group profile.
<br /><br />
<b>Main Points Raised in C&TA Calls:</b>
<br /><br />
Philip Brennan:
<ul>
<li>Implementation reality (Labs → GP): using Observation as grouper (EU pattern), back adopting R6 Observation.organizer Boolean; progressing in production.</li>
</ul>
Kevin Sprague:
<ul>
<li>Will align with Phil offline; later slides include related R6 back port work in scope.</li>
<li>Agreed: build a roadmap via FIRE Board; this sprint is alignment; process to be revamped.</li>
</ul>
Heather Wallace:
<ul>
<li>NHS Wales doing observation grouping for child growth charts—flag for future.</li>
</ul>
Charlie McCay:
<ul>
<li>Capture these real implementations and workarounds in the pack for community benefit.</li>
</ul>
Andrew Perry:
<ul>
<li>Pressed that imminent implementations should raise priority; advocated a roadmap to address pressing issues.</li>
</ul>
</td>
<td>Proposed Out of Scope</td>
</tr>
<tr>
<td>{{pagelink:Issue-9}}</td>
<td><a href="https://simplifier.net/hl7fhirukcorer4/extension-ukcore-codingsctdescdisplay" target="_blank">Extension-UKCore-CodingSCTDescDisplay</a> (Extension)</td>
<td>Implementation Guide</td>
<td>UK Core Development Team</td>
<td>The IG guidance states that if the sct-descId is sent,
then the UK Core sctdescDisplay SHALL be used.</td>
<td>
<b>Initial Proposal:</b>
<br /><br />
The requirement should be changed from SHALL to MAY.

Click <a href="https://simplifier.net/guide/UK-Core-Implementation-Guide-STU3-Sequence/Home/Guidance/CodeableConcept-Guidance?version=current#Sending-a-SNOMED-CT-Description-ID-that-is-not-the-preferred-term" target="_blank">here</a>

<br /><br />
<b>Main Points Raised in C&TA Calls:</b>
<br /><br />
Kevin Sprague:
<ul>
<li>There’s a live vendor issue suggesting UK Core diverges from base FHIR behavior; reviewing; may need options (including deprecation).</li>
</ul>
Ann Wrightson:
<ul>
<li>While under review, relaxing to MAY helps implementers and reduces harm.</li>
</ul>
Charlie McCay:
<ul>
<li>This should be solved internationally (HL7 + SNOMED), not by a UK only extension; avoid extending extensions; basic FHIR–SNOMED integration must be straightforward.</li>
</ul>
Ryan May:
<ul>
<li>Context: the need was to send a non preferred term text alongside the conceptId; past misuse included sending descriptionIds as codes.</li>
</ul>
</td>
<td>Proposed In Scope</td>
</tr>
<tr>
<td>{{pagelink:Issue-10}}</td>
<td>sct-descid</td>
<td>Implementation Guide</td>
<td>UK Core Development Team</td>
<td>Use of sct-descId for mapping and READ codes. The extension is only for showing a non-preferred term within SCT, linking it with the preferred term. If using other codes systems and mapping to SCT then both would go in seperate .coding elements, with userSelected chosen to represent the original.</td>
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
<td>Proposed In Scope</td>
</tr>
<!-- <tr>
<td>{{pagelink:Issue-11}}</td>
<td>N/A</td>
<td>N/A</td>
<td>N/A</td>
<td>N/A</td>
<td>N/A</td>
<td>Always Out of Scope - Development Done</td>
</tr> -->
<!-- <tr>
<td>{{pagelink:Issue-12}}</td>
<td>Downdown List</td>
<td>Implementation Guide</td>
<td>UK Core Development Team</td>
<td>Some Resources not showing in correct category in dropdown</td>
<td>Propose removing the banner and sticking to the index page only to find profiles.</td>
<td>Proposed In Scope - Development Done</td>
</tr> -->
<tr>
<td>{{pagelink:Issue-13}}</td>
<td>Parameter</td>
<td>FHIR Asset</td>
<td>UK Core Development Team</td>
<td>IG Publishing tool gives the following warning if you haven’t set the Snomed CT edition.</td>
<td>
<b>Initial Proposal:</b>
<br /><br />
Propose to include SNOMED version in Parameter resource.
<br /><br />
<b>Main Points Raised in C&TA Calls:</b>
<br /><br />
Kevin Sprague:
<ul>
<li>Not hurting anyone now; needs analysis and agreement—put on roadmap.</li>
</ul>
</td>
<td>
Proposed Out of Scope
</td>
</tr>
<!-- <tr>
<td>{{pagelink:Issue-14}}</td>
<td><a href="https://simplifier.net/hl7fhirukcorer4/ukcore-encounter" target="_blank">UKCore-Encounter</a> (Profile)</td>
<td>Mapping</td>
<td><a href="https://simplifier.net/hl7fhirukcorer4/ukcore-encounter/~issues/3303" target="_blank">Simplifier Issue</a></td>
<td>Inconsistency between mapping and external specifications.</td>
<td>No proposal stated.</td>
<td>Proposed Out of Scope</td>
</tr> -->
<!-- <tr>
<td>{{pagelink:Issue-15}}</td>
<td><a href="https://simplifier.net/hl7fhirukcorer4/ukcore-encounter" target="_blank">UKCore-Encounter</a> (Profile)</td>
<td>Binding</td>
<td><a href="https://simplifier.net/hl7fhirukcorer4/ukcore-encounter/~issues/3302" target="_blank">Simplifier Issue</a></td>
<td>The binding is currently to https://simplifier.net/hl7fhirukcorer4/valueset-ukcore-dischargedestination.</td>
<td>Should be bound to hospitalization.destination</td>
<td>Proposed In Scope</td>
</tr> -->
<tr>
<td>{{pagelink:Issue-16}}</td>
<td><a href="https://simplifier.net/hl7fhirukcorer4/ukcore-encounter" target="_blank">Encounter</a> (Profile), <a href="https://simplifier.net/hl7fhirukcorer4/ukcore-appointment" target="_blank">Appointment</a> (Profile), <a href="https://simplifier.net/hl7fhirukcorer4/ukcore-slot" target="_blank">Slot</a> (Profile)</td>
<td>Binding</td>
<td><a href="https://simplifier.net/hl7fhirukcorer4/ukcore-appointment/~issues/3273" target="_blank">Simplifier Issue</a></td>
<td>Appointment/Slot binds to http://terminology.hl7.org/CodeSystem/service-type</td>
<td>
<b>Initial Proposal:</b>
<br /><br />
Propose to bind to https://fhir.hl7.org.uk/ValueSet/UKCore-CareSettingType
(Uses SNOMED CT UK Refset with fully specified name 'Services simple reference set’) as it does in Encounter
<br /><br />
<b>Main Points Raised in C&TA Calls:</b>
<br /><br />
Kevin Sprague:
<ul>
<li>Binding strength likely preferred (advisory, not enforced); this improves guidance without mandating.</li>
</ul>
</td>
<td>Proposed In Scope</td>
</tr>
<tr>
<td>{{pagelink:Issue-17}}</td>
<td><a href="https://simplifier.net/hl7fhirukcorer4/valueset-ukcore-bloodpressure-systolic" target="_blank">UKCore-BloodPressure-Systolic</a> (ValueSet)</td>
<td>Terminology Concepts</td>
<td><a href="https://simplifier.net/hl7fhirukcorer4/valueset-ukcore-bloodpressure-systolic/~issues/3296" target="_blank">Simplifier Issue</a></td>
<td>Concepts to use when recording central venous pressure.
Currently if you are representing a CVP or other invasive blood pressures,
which appear to be in scope, there are no appropriate concepts to record
the systolic and diasolic pressures. It would not be correct to use
271649006 &verbar; Systolic blood pressure (observable entity)as this is not
what it is. So to represent correctly you would need to use a concept
specifically for invasive blood pressure.</td>
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
<td>Proposed In Scope</td>
</tr>
<tr>
<td>{{pagelink:Issue-18}}</td>
<td><a href="https://simplifier.net/hl7fhirukcorer4/ukcore-observation-vitalsigns-bloodpressure" target="_blank">UKCore-Observation-VitalSigns-BloodPressure</a> (Profile)</td>
<td>Terminology Concepts</td>
<td><a href="https://simplifier.net/hl7fhirukcorer4/ukcore-observation-vitalsigns-bloodpressure/~issues/3297" target="_blank">Simplifer Issue</a></td>
<td>There are 3 SNOMED CT codes used in this model top level to record the type of BP - then 2 codes to record the systolic and diastolic results/values.</td>
<td>
<b>Initial Proposal:</b>
<br /><br />
For each top code it needs to be validated that there are clinically validated systolic concepts defined. Or even if the concept of systolic and diastolic is valid for CVP and invasive blood pressures. This need work with an expert in intensive care to validate.
<br /><br />
<b>Main Points Raised in C&TA Calls:</b>
<br /><br />
Ian McNicoll:
<ul>
<li>Keep the top level “BP” code generic (as a grouper); actual semantics live in systolic/diastolic children; trim the top level value set.</li>
</ul>
Ann Wrightson:
<ul>
<li>Document intended use as vital signs (ward/GP) to avoid scope creep.</li>
</ul>
Kevin Sprague:
<ul>
<li>Treat 17 & 18 together; align with existing work (Ian’s).</li>
</ul>
</td>
<td>Proposed In Scope</td>
</tr>
<tr>
<td>{{pagelink:Issue-19}}</td>
<td><a href="https://simplifier.net/hl7fhirukcorer4/ukcore-observation-averagebloodpressure" target="_blank">UKCore-Observation-AverageBloodPressure</a> (Profile)</td>
<td>Terminology Concepts</td>
<td><a href="https://simplifier.net/hl7fhirukcorer4/ukcore-observation-averagebloodpressure/~issues/3300" target="_blank">Simplifier Issue</a></td>
<td>The SNOMED CT concepts identified include invasive blood pressures
but believe this should not be in scope. If they are then as for #3297 the concepts need validation with intensive care experts to validate that the concepts for the values and the units are all available.</td>
<td>
<b>Initial Proposal:</b>
<br /><br />
If they are then as for #3297 the concepts need validation with intensive care experts to validate that the concepts for the values and the units are all available.
<br /><br />
<b>Main Points Raised in C&TA Calls:</b>
<br /><br />
Kevin Sprague:
<ul>
<li>Will fall out naturally once BP scoping is corrected.</li>
</ul>
</td>
<td>Proposed In Scope</td>
</tr>
<!-- <tr>
<td>{{pagelink:Issue-20}}</td>
<td>N/A</td>
<td>N/A</td>
<td>N/A</td>
<td>N/A</td>
<td>N/A</td>
<td>Always Out of Scope - Development Done</td>
</tr> -->
<tr>
<td>{{pagelink:Issue-21}}</td>
<td><a href="https://simplifier.net/hl7fhirukcorer4/valueset-ukcore-allergymanifestation" target="_blank">UKCore-AllergyManifestation</a> (ValueSet)</td>
<td>Terminology</td>
<td><a href="https://simplifier.net/hl7fhirukcorer4/valueset-ukcore-allergymanifestation/~issues/3317" target="_blank">Simplifier Issue</a></td>
<td>Health issues simple reference set (1127581000000103) is retired.</td>
<td>
<b>Initial Proposal:</b>
<br /><br />
No proposal stated.
<br /><br />
<b>Main Points Raised in C&TA Calls:</b>
<br /><br />
Ann Wrightson:
<ul>
<li>Asked to replace “seems retired” with firm evidence; document how retirement is confirmed.</ul>
</li>
Andrew Perry:
<ul>
<li>Confirmed retirements; explained background (large, hard to maintain refsets; alternatives exist).</li>
<li>Can suggest an alternative refset/binding if needed.</li>
<li>IPS sets are too small/coarse for manifestations like rash subtypes; not ideal for UK clinical detail.</li>
</ul>
Ian McNicoll:
<ul>
<li>Suggested considering IPS value sets for alignment.</li>
</ul>
Kevin Sprague:
<ul>
<li>Illustrates why out of scope: needs proper multi party terminology session; add to roadmap.</li>
</td>
<td>Proposed Out of Scope</td>
</tr>
<tr>
<td>{{pagelink:Issue-22}}</td>
<td><a href="https://simplifier.net/hl7fhirukcorer4/ukcore-observation-tobaccoconsumption" target="_blank">UKCore-Observation-TobaccoConsumption</a> (Profile), <a href="https://simplifier.net/hl7fhirukcorer4/valueset-ukcore-tobaccoconsumption" target="_blank">UKCore-TobaccoConsumption</a> (ValueSet)</td>
<td>Modelling</td>
<td>UK Core Development Team</td>
<td>tobaccoConsuption profile only allows valueQuantity, but SNOMED CT UK has codes such as 160603005 &verbar; Light cigarette smoker (1-9 cigs/day) (finding)&verbar;</td>
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
<td>Proposed In Scope</td>
</tr>
</table> 