

Mandatory Verification, Traceability & Archival Requirement

Now after the execution, you must produce a Verification & Change Report. This is mandatory.

Report Metadata (Required)

At the very top of the report, include:
	•	Title: Verification & Change Report — <Task Name>
	•	Date: <YYYY-MM-DD>
	•	Status: Completed
	•	Scope: <Brief scope statement>

⸻

Report Structure (Do Not Alter)

1. Files Touched
	•	Explicit list of every file created, modified, or deleted
	•	For each file:
	•	Why it was touched
	•	What changed (high-level, no diffs)

⸻

2. Security Verification
Explicitly confirm:
	•	No API keys or secrets exist in client-side code
	•	No secrets are present in the frontend build output
	•	All sensitive logic remains server-side

Also state how this was verified:
	•	Build output inspection
	•	Config review
	•	Manual search
	•	Other concrete method

If anything was not verified, mark it UNVERIFIED.

⸻

3. Scope Compliance Check
Explicitly confirm:
	•	No new product features were added
	•	No UI/UX changes were made
	•	No work beyond the defined task scope was performed

If anything outside scope was touched:
	•	List it explicitly
	•	Justify why it was unavoidable

⸻

4. Truthfulness Audit
List any remaining logic that is:
	•	Heuristic
	•	Placeholder
	•	Simulated
	•	Not fully backed by real data

For each:
	•	Removed
	•	Clearly labeled
	•	Intentionally left untouched (with reason)

⸻

5. Build & Run Status
	•	Exact steps to build and run the project
	•	Explicit confirmation that:
	•	Build succeeds
	•	Runtime starts without errors

⸻

6. Risk Residuals
	•	Known risks that remain
	•	Why each risk is acceptable at this phase
	•	No minimization or hand-waving

⸻

Archival Requirement (Mandatory)

After generating the report:
	1.	Save it verbatim as a Markdown file in:

/documentation/implementation/

	2.	File naming format:

YYYY-MM-DD_verification-change-report_<short-task-name>.md

	3.	Do not overwrite any existing documentation.
Documentation is append-only.

⸻

Rules
	•	No vague statements
	•	No assumptions
	•	Precision over brevity
	•	Anything not verified must be labeled UNVERIFIED
	•	If this report is missing or not archived, the task is incomplete

⸻

This version is short, enforceable, auditable, and now self-archiving.
