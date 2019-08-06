# Worthy v.1 History

## About

The whole process of Worthy v. 2 has started as a revival of the Worthy - Transparent Personal Finance App (iOS) by Kujunda Seda OÜ. The former was abandoned in about 2017, although it is still enjoyed by users even 2 years later. With Worthy v. 2 we aim to build on the legacy of the classic app, spread it to more platforms, add new features and streamline the user experience.

The classic Worthy app has the following features:

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

## Transactions

1. Create a transaction (with the following properties):
	- Transaction account (implicit, a transaction belongs to an account)
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
4. Automatic transfer amount according to exchange rate for date
5. Create account adjustment transaction specifying balance for date and autocaluculated amount
6. Add/delete category when selecting it for a transaction


## Spending

1. Group transactions by period and by category
	- sum is calculated from amounts converted to base currency based on exchange rates history
2. See all transactions for selected category
3. Merge multiple categories into single one (modifying all included transactions)
4. Delete category without deleting transactions
5. Group categories by income and expense automatically

## Currencies

1. Add a new currency (the only property is Name)
2. Edit a currency (i.e. it's Name)
3. Delete a currency
4. Add an exchange rate historic value
5. Edit an exchange rate historic value
6. Remove an exchange rate historic value
7. Change base currency

## Conclusion

The above feature set may serve as the basis for the product plan of Worthy v. 2, adjusted to the requirements set for the new project.



