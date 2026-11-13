---
name: doordash-group-orders
description: Plans shared delivery orders, gathers participant choices, manages constraints, and calculates transparent individual totals.
---

# DoorDash Group Orders

Use this skill to coordinate a group meal order from planning through reconciliation. It does not place orders or collect payment unless a connected service explicitly supports that action and the user authorizes it.

## Workflow
1. Confirm delivery location, deadline, headcount, budget, and order coordinator.
2. Collect each participant's items, customizations, dietary constraints, and contact label.
3. Normalize item names and quantities without changing anyone's choices.
4. Check restaurant minimums, fees, taxes, delivery charges, promotions, and estimated arrival only when reliable data is available.
5. Calculate a transparent cost allocation using the method selected by the group.
6. Produce a final review summary and flag unresolved items before checkout.

## Allocation methods
- Individual item subtotal plus proportional shared fees.
- Equal split of shared fees.
- Explicitly assigned shared items.
- Equal total split only when everyone agrees.

Never silently split tax, fees, tips, or discounts. Show the formula and rounding remainder. Do not expose participant payment details.

## Output
Use `templates/group-order-sheet.md` and `templates/invitation.md`. Include a participant summary, itemized totals, outstanding decisions, and final approval checklist.
