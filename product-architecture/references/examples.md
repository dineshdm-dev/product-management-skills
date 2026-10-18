# Authored Examples

These are illustrative outputs written for this skill, not model-run results.

## Complete case: permit application status

**Input:** “A city service receives permit applications. Applicants need status; reviewers can request changes; documents are stored by another system.”

**Illustrative output:** Model an Application as the primary object, with Document as a referenced external record and Review Request as a first-class event linked to an application. The city service owns application status and review history; the document system owns file content. States include draft, submitted, changes-requested, under-review, approved, and closed. Applicants can see only their application and requests addressed to them. This preserves an auditable history and avoids copying document authority.

## Difficult case: field versus object

**Input:** “Add a `blocked` checkbox to shipments.” Different blocks have owners, expiry, and resolution history.

**Illustrative output:** A checkbox loses the reason, owner, lifecycle, and history needed for action. Model a Blocker object related to a shipment; derive a blocked status for list views. Open question: can several blockers be active at once?
