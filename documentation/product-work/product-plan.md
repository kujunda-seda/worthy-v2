# Product Plan

## History
Discovering https://github.com/ledger/ledger project we decided to simplify initial plan of a full-feature app into client-only app using the ledger format.

## Purpose of the app
Simplified input of personal finance transactions from phone.

## MVP Milestones
1. Select ledger file (from a single source)
2. Parse ledger file
3. Show all ledger entries
4. Define fully parsed / editable entries
5. Edit entries (saved into source)
6. Add entries (saved into source)
7. Delete entries (saved into source)
8. Export file into a different source

## Notes
No reporting is implied within the client for now. Reporting is done via ledger-cli. As the most complex part is parsing the file it should be researched first, maybe a good solution already exists.