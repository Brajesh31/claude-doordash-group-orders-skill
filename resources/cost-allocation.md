# Group Order Cost Allocation

Let participant i have item subtotal Sᵢ, total item subtotal S, shared fee pool F, and assigned discount Dᵢ.

## Proportional shared fees
If S > 0:
`feeᵢ = round(F × Sᵢ / S, 2)`

Then:
`totalᵢ = Sᵢ + feeᵢ - Dᵢ`

## Equal shared fees
For n participants:
`base = floor((F / n) × 100) / 100`

Assign any remaining cents deterministically, for example by participant order, and disclose the rule.

## Discount handling
- Item-specific discount: assign to the participant who ordered that item.
- Order-wide discount: allocate proportionally unless the group chooses another method.
- Promo eligibility or caps: use the actual checkout breakdown, not an assumed discount.

Always reconcile participant totals to the checkout grand total. If they differ, show the discrepancy rather than hiding it in rounding.
