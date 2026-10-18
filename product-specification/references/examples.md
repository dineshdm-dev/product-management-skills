# Authored Examples

These are illustrative outputs written for this skill, not model-run results.

## Complete case: missing-document upload

**Input:** “Applicants need to upload documents requested during a loan review. Reviewers need to confirm receipt.”

**Illustrative output:** Scope: applicants view outstanding document requests and upload a replacement; reviewers see submission time and can mark it accepted or request another version. Non-goal: automatic document approval. Acceptance criterion: given an authenticated applicant has an open request, when an allowed file is uploaded, then the request shows `submitted`, records submission time, and is visible to assigned reviewers. Open decision: permitted file types and retention policy.

## Difficult case: vague requirement

**Input:** “Make the application page intuitive.”

**Illustrative output:** This is not observable. Clarify the task the applicant must complete, current failure evidence, required information, and error recovery. Do not convert a subjective adjective into a commitment.
