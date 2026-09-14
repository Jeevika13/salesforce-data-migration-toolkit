# Post-Migration Validation Checklist

- [ ] Record counts match between source extract and target org (per object)
- [ ] Spot-check 5–10% of records for field-level accuracy against source
- [ ] Relationship integrity verified (e.g., every Contact has a valid Account lookup)
- [ ] Picklist values all resolved — no blank/"Other" values from failed remaps
- [ ] Required validation rules did not silently block records (check load error log)
- [ ] Duplicate rules run clean — no unexpected duplicate flags
- [ ] Reports/dashboards referencing migrated objects return expected totals
- [ ] Business stakeholder sign-off (UAT) obtained before cutover
