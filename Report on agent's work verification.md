## Mandatory Verification & Traceability Requirement

At the end of execution, you must produce a **Verification & Change Report** with the following structure. This is not optional.

---

### 1. Files Touched
- Explicit list of every file **created**, **modified**, or **deleted**
- For each file, specify:
  - **Why** it was touched
  - **What** changed (high-level explanation, not raw diffs)

---

### 2. Security Verification
You must explicitly confirm all of the following:
- No API keys or secrets exist in client-side code
- No secrets are present in the final frontend bundle
- All sensitive logic (LLM calls, credentials, config) is server-side only

Also state **how** this was verified:
- Build output inspection
- Config review
- Manual search
- Other concrete method

If something was not verified, it must be marked **UNVERIFIED**.

---

### 3. Scope Compliance Check
Explicitly confirm:
- No new product features were added
- No UI/UX changes were made unless strictly required for security
- No Phase 2 or Phase 3 work was started

If **anything** outside the defined scope was touched:
- List it clearly
- Justify why it was unavoidable

---

### 4. Truthfulness Audit
List any remaining logic that is:
- Heuristic
- Simulated
- Placeholder
- Non-backed by real data

For each item, state whether it was:
- Removed
- Clearly labeled
- Intentionally left untouched (with reason)

---

### 5. Build & Run Status
- Exact steps to run the system after changes
- Confirmation that:
  - The project builds successfully
  - The project runs without runtime errors

---

### 6. Risk Residuals
- Explicit list of known risks that still remain
- Why each risk is acceptable **at this phase**
- Risks must not be minimized or hand-waved

---

### Format & Accountability Rules
- No vague statements (e.g., “cleaned up”, “fixed issues”)
- No assumptions
- Precision over brevity
- If something cannot be verified with certainty, mark it **UNVERIFIED**

Failure to provide this report means the task is incomplete.
