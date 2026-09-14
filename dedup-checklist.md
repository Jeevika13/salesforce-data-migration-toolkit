# Deduplication Checklist

Used before loading Leads/Contacts into Salesforce.

1. **Exact match pass** — group records by lowercased, trimmed Email. Flag duplicates.
2. **Phone match pass** — normalize all phone numbers to a single format, group by number. Flag duplicates not already caught by email match.
3. **Fuzzy name match** — for records with no email/phone match, compare Name + Company using a similarity threshold (e.g., Levenshtein distance) and manually review flagged pairs.
4. **Survivorship rule** — when merging, keep the record with the most recent Last Activity Date; carry over any populated fields the survivor is missing from the loser record.
5. **Merge log** — record every merge decision (winner ID, loser ID, reason) in a migration log for audit purposes.
6. **Post-load re-check** — run a duplicate rule report in Salesforce after load to catch anything missed pre-load.
