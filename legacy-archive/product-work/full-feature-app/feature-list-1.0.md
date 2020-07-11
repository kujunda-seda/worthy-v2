# Worthy v. 2 Feature List

Because Worthy v.1 is already an accomplished personal finance app we have decided to base the feature list of the new app on the existsing feature set of Worthy with some modifications.

The new Worthy v. 2 app will have the following feature set for version 1.0

## Accounts

1. Create an account (with the following properties):
	- Account name
	- Account group
	- Account currency
	- Initial balance
2. Edit an account (modify the above properties)
3. Delete an account
4. Add/rename account group
5. Reorder account groups
6. Total net worth calculation in chosen currency using current exchange rates
7. **(new feature)** Archive (hide) account
8. **(new feature)** Reorder accouts within a group
9. **(new feature)** New account property - "include in Net worth calculation"

## Transactions

1. Create a transaction (with the following properties):
	- Transaction account ~~(implicit, a transaction belongs to an account)~~
	- Transaction date
	- Transaction amount
	- Transaction type:
		- Income
		- Expense
		- Transfer
	- Transaction category (if type is Income / Expense)
	- Transfer account (if type is Transfer)
	- Transfer amount (if Transfer account is in another currency)
	- Transaction memo
2. Edit a transaction
3. Delete a transaction
4. ~~Automatic transfer amount according to exchange rate for date~~
5. Create account adjustment transaction specifying balance for date and autocaluculated amount
6. Add/delete category when selecting it for a transaction
7. **(new feature)** Sort categories and accounts in transaction edit screen according to how often they are used
8. **(new feature)** Predictive input in category/account selection screen (as the user begins typing out the category/account name, the list of available categories gets filtered out)

## Spending

1. Group transactions by period and by category
	- sum is calculated from amounts converted to base currency based on exchange rates history
2. See all transactions for selected category
3. Merge multiple categories into single one (modifying all included transactions)
4. Delete category without deleting transactions
5. Group categories by income and expense automatically
6. Filter transactions by date

## Currencies

1. Add a new currency (the only property is Name)
2. Edit a currency (i.e. it's Name)
3. Delete a currency
4. ~~Add an exchange rate historic value~~
5. ~~Edit an exchange rate historic value~~
6. ~~Remove an exchange rate historic value~~
7. Set/change base currency
8. **(new feature)** Automatic currency history (for net worth and spending calculations)

## Other new features

1. **(new feature)** Multi-user support
2. **(new feature)** Backup / import / export of raw data

## Conclusion

We will need to develop an architectural solution based on the above feature set.
