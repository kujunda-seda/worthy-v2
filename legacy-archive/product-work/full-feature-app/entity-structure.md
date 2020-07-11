# Entity structure
This document contains classification of important source data that has to be permanently stored (e.g. in a database). It is to be converted into scheme during implementation.

## Entities with properties

### Entries
- memo
- date
- order in date
- transcations

### Transactions
- account debited
- account credited
- amount

### Accounts
- name
- type
- currency
- group
- order in group

### Groups
- name
- order in list

### Account types
- name

### Currencies
- ISO code

### Exchange rates
- exchange from currency
- exchange into currency
- rate
- date

### User parameters
- base currency
> Implementation detail: `base currency` information can be derived from income/expense accounts' currency as they all should have the same currency according to chosen accounting model.
