**prompt**

In July 2024, the White House Office of Science and Technology Policy released a final “Guidelines for Research Security Programs at Covered Institutions” memo, instructing federal agencies to implement research security policies that meet specific requirements.  Can you recommend what documentation and policies we might need to show that we are in compliance with this?

**answer**

You’ll want to be able to show (1) that you have a formal “Research Security Program” that matches the OSTP memo, and (2) that you operate it in practice (policies + evidence). I’ll lay this out by OSTP’s required elements plus some cross-cutting pieces.

Quick context: OSTP’s July 9, 2024 memo says that covered institutions (those getting >$50M/year in federal S&E funding) must certify they have a research security program that includes four elements: cybersecurity, foreign travel security, research security training, and export control training, plus safeguards against discrimination.  ￼

⸻

1. Overarching “Research Security Program” documentation

You’ll almost certainly want:
	1.	Research Security Program Policy (top-level doc)
A single, approved policy that:
	•	States that your institution is implementing OSTP’s Guidelines for Research Security Programs at Covered Institutions under NSPM-33 and CHIPS.  ￼
	•	Defines “covered institution” and “covered individuals” using the OSTP definitions.  ￼
	•	States that your program includes (a) cybersecurity, (b) foreign travel security, (c) research security training, and (d) export control training.
	•	Explains your risk-based approach and the principle of non-discrimination (no targeting or profiling by nationality, race, etc.), as required in the guidelines.  ￼
	2.	Governance & roles
	•	A short RSP Governance Charter that:
	•	Identifies the responsible office(s): CIO/IT security, export control office, research administration, HR, legal/compliance.
	•	Names a Research Security Officer / committee and their responsibilities (policy oversight, assessments, training oversight, incident escalation).
	•	An org chart or RACI matrix showing who does what for each of the four elements.
	3.	Crosswalk to OSTP Guidelines
	•	A 1–2 page “OSTP RSP Crosswalk” table that maps:
	•	OSTP paragraph/requirement →
your policy/SOP/training →
system or record that proves it’s being done.
	•	This is extremely useful when agencies formalize their own requirements.
	4.	Certification language & process
	•	Internal procedure that says:
	•	Who signs the institutional certification to federal agencies.
	•	Where they pull evidence from (logs, training reports, etc.).
	•	A standard certification template (even if agencies later impose their own) so you’re ready when NIH/NSF etc. ask you to attest.  ￼
	5.	Non-discrimination safeguards
	•	Either:
	•	Incorporate into the Research Security Program Policy, or
	•	Reference existing EEO / non-discrimination policies and explain how they apply to research security practices (e.g., travel review, collaboration review).
	•	You’ll need to be able to certify you’ve implemented safeguards to avoid discriminatory application of research security measures.  ￼

⸻

2. Cybersecurity (Element #1)

OSTP doesn’t mandate a specific framework, but points to NIST work (e.g., NIST IR 8481) and allows use of other NIST/cyber resources.  ￼

Core documents to have ready:
	1.	Information Security Policy
	•	Align with a recognized framework (e.g., NIST CSF / 800-171 / 800-53, or NIST IR 8481 for research).  ￼
	•	Explicitly cover research systems: storage, HPC, LIMS, collaboration tools, cloud platforms, archives.
	2.	System Security Plans / Technical Standards
	•	Access control & MFA standard (accounts, role-based access).
	•	Network segmentation and remote access rules.
	•	Vulnerability management & patching SOP.
	•	Backup & recovery standards for research data.
	3.	Incident Response Plan
	•	A documented incident response playbook that:
	•	Includes scenarios like data exfiltration, compromised PI account, or suspected foreign interference with research systems.
	•	Defines how and when to escalate to federal agencies (as required by terms & conditions).
	4.	Data classification & handling
	•	A data classification policy that distinguishes:
	•	Public, internal, confidential, and regulated data (CUI, export-controlled tech, human subjects data, etc.).
	•	Handling rules for each class, especially when sharing internationally.
	5.	Vendor / third-party risk
	•	A simple third-party risk management procedure for research IT services, including cloud collaborations, code repositories, external data platforms.

Evidence to keep on hand: recent risk assessment, penetration test or vulnerability scan results, examples of system security plans, incident logs (de-identified), change control or patching records.

⸻

3. Foreign Travel Security (Element #2)

OSTP requires periodic foreign travel security training and a travel reporting program for certain federally funded R&D when agencies determine risk warrants it.  ￼

Key docs:
	1.	International Travel Policy (Research-focused)
	•	Scope: who is covered (faculty/PI equivalents, postdocs, staff, students on federal awards).
	•	Requirements:
	•	Pre-travel registration/approval if travel is related to federally funded R&D.
	•	Use of institution-managed devices for sensitive work, secure VPN, etc.
	•	Prohibitions or approvals for taking export-controlled data or equipment.
	2.	Foreign Travel Security Training
	•	A training policy that:
	•	Specifies who must take foreign travel security training.
	•	Sets frequency (OSTP says at least once every six years after a federal module becomes available).  ￼
	•	Training content (or link to federal module when NSF’s module is rolled out).
	3.	Travel Reporting Program
	•	Written procedure describing:
	•	How international travel by covered individuals is logged (system, who enters it, what data).
	•	How you identify which trips are subject to additional reporting under award terms.
	•	A form/template (or system screenshot) showing required fields.

Evidence: exports from your travel registry, completion reports from foreign travel training module, examples of risk reviews for specific trips.

⸻

4. Research Security Training (Element #3)

OSTP allows two ways: use the NSF research security training modules (or successor) or provide your own equivalent training that includes explicit examples of risky behavior and emphasizes the value of open global collaboration.  ￼

Documentation to prepare:
	1.	Research Security Training Policy
	•	Who counts as a “covered individual” at your institution (e.g., anyone named on a federal R&D award, plus certain administrators).
	•	Timing: required at onboarding + refresher interval (e.g., every 3 years, or aligned with federal requirements).
	•	Acceptable training options (NSF modules vs. institutional modules).
	2.	Training Content / Program Description
	•	If you use NSF’s Research Security Training Modules, reference them and document that they are mandatory.  ￼
	•	If you develop your own:
	•	Syllabi or slide decks with:
	•	Examples of behaviors that led to improper or illegal transfer of R&D (cases from DOJ/agency guidance, etc.).
	•	How to disclose outside support, affiliations, and foreign collaborations appropriately.
	•	Emphasis on non-discrimination and the importance of international collaboration.
	3.	Training Records
	•	Integration with your LMS/HR system.
	•	Ability to run a completion report by person, by award, and by date to support agency audits.

⸻

5. Export Control Training (Element #4)

OSTP says you must require export control training for covered individuals who perform R&D involving export-controlled technologies, and you may either use BIS/DDTC training or institution-developed modules that cover U.S. export control requirements and processes for reviewing foreign sponsors/collaborators.  ￼

Core docs:
	1.	Export Control & Sanctions Policy
	•	Identifies your Export Control Officer/Empowered Official.
	•	References EAR, ITAR, OFAC, and relevant institutional procedures.
	•	Links export control to:
	•	Sponsor and collaborator review.
	•	Technology control plans in high-risk labs.
	•	Shipping and data-sharing procedures.
	2.	Export Control Training Program
	•	Policy specifying:
	•	Who is required to complete export control training (e.g., PIs of certain grants, lab staff in regulated labs, certain IT admins).
	•	Training content and recurrence.
	•	Either:
	•	Documentation that you use BIS/DDTC trainings, or
	•	Internal training materials covering:
	•	Basics of export control.
	•	Deemed exports and foreign nationals in labs.
	•	Review of foreign sponsors and collaborators.
	3.	Technology Control Plans (TCPs) & SOPs
	•	Templates for TCPs for labs handling export-controlled tech.
	•	Procedures for physical and IT access controls in those labs.

Evidence: TCP examples (sanitized), export training completion logs, records of export reviews for specific awards/shipment approvals.

⸻

6. Related areas that strengthen your compliance story

These aren’t explicitly one of the four elements, but they’ll be important for agencies and align with NSPM-33, CHIPS, and related OSTP guidance.  ￼
	1.	Disclosure & other support policies
	•	Policies and forms for:
	•	Outside professional activities and foreign affiliations.
	•	Current & pending/other support.
	•	Prohibitions on participation in malign foreign talent recruitment programs.
	•	Documentation that your systems/forms are updated to match the common disclosure requirements as agencies converge on them.
	2.	Visitor & access controls
	•	Lab visitor policy (badging, escorts, visit logs).
	•	Onboarding/offboarding checklists ensuring timely removal of physical and IT access.
	3.	Collaboration & data-sharing agreements
	•	Templates for:
	•	Data Use Agreements, MTAs, collaboration MOUs, subaward agreements.
	•	Language about:
	•	Export control, data security, and disclosure obligations.
	•	Restrictions on sharing with entities in countries of concern when applicable.
	4.	Incident management & reporting
	•	A research security incident SOP that ties together:
	•	Cyber incidents,
	•	Suspected violations of export control,
	•	Undisclosed foreign affiliations/other support.
	•	Link to whistleblower / reporting channels.
	5.	Program evaluation
	•	A brief annual review process for your research security program:
	•	What metrics you track (training completion, incident counts, travel reviews, etc.).
	•	How you adjust policies in response to new OSTP or agency guidance.

⸻

7. Practical “starter checklist”

If you want a concrete work plan, you could aim to have, in one shared folder:
	1.	Top-level
	•	✅ Research Security Program Policy (with non-discrimination section)
	•	✅ Governance / RSP charter & RACI
	•	✅ OSTP crosswalk matrix
	•	✅ Draft institutional certification language
	2.	Four elements
	•	✅ InfoSec policy + incident response plan + data classification standard
	•	✅ Foreign travel policy + training documentation + travel reporting procedure
	•	✅ Research security training policy + content + completion reports
	•	✅ Export control policy + training program + TCP template and example
	3.	Supporting
	•	✅ Disclosure/other support and FTRP policy
	•	✅ Visitor/access control procedures
	•	✅ Example DUAs/MTAs with security language
	•	✅ Research security incident SOP
	•	✅ Annual review / metrics summary

⸻

If you’d like, you can tell me a bit about your current policy landscape (e.g., “we already have X, Y, Z”) and I can turn this into a very specific gap-analysis list for your institution.

(Standard disclaimer: this is general informational guidance based on OSTP’s public memo and related commentary and is not legal advice; you’ll want institutional counsel/compliance to review before finalizing.)
