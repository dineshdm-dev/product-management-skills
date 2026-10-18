# Authored Examples

These are illustrative outputs written for this skill, not model-run results.

## Complete case: interrupted meal-order change

**Input:** “A customer can change a meal order until preparation starts. People complain that the button disappears.”

**Illustrative output:** Keep order state visible: `change available until 4:00 PM`, `change window closed`, or `preparing`. Before the deadline, show the change action beside the chosen meal and confirm the effect. After it closes, replace the hidden button with a concise reason and a support path if policy allows. Announce state changes programmatically so screen-reader users receive the same feedback.

## Difficult case: hiding controls

**Input:** “Hide cancellation settings to make setup simpler.” Administrators are accountable for recurring charges.

**Illustrative output:** Hiding the setting reduces visual load but conceals a consequential commitment. Keep it discoverable in setup or confirmation, use plain language about the charge effect, and provide a recovery path.
