# Salesforce Data Migration Toolkit

Reusable templates and approach for Salesforce data migration projects — mapping, cleansing, deduplication, and post-load validation, based on real estate CRM migrations (property/listing/lead data from legacy systems into Salesforce).

## Contents
- `field-mapping-template.csv` — source-to-target field mapping template used before any load
- `dedup-checklist.md` — deduplication approach for Leads/Contacts by email + phone fuzzy match
- `post-migration-validation.md` — checklist run after every load

## Migration process followed
1. **Discovery** — inventory source fields, identify required vs. optional target fields
2. **Mapping** — fill in `field-mapping-template.csv`, flag transformations (e.g., picklist value remaps)
3. **Cleansing** — standardize phone/email formats, trim whitespace, dedupe before load
4. **Load** — Data Loader / Bulk API insert in batches, staging environment first
5. **Validation** — record count reconciliation, spot-check field accuracy, relationship integrity (e.g., Contact → Account)
6. **Sign-off** — UAT with business stakeholders before production cutover
