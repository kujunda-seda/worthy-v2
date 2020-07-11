# Product Notes on Accounting
Worthy will use double-entry accounting system. All double-entry logic will be hidden under the hood so that user will experience foolproof, convenient and natural input method. Reasons behind this decision:

1. easier to extend/modify in the future
2. error-controlled by equation

## Account types
The following account types will be present in the database, but will not be seen by the user directly. British/American classification of account types is given in brackets.

1. Income (Nominal / Income)
2. Expense (Nominal / Expense)
3. Assets (Real / Assets)
4. Loans (Personal / Assets or Liabilities)
5. Currency (Nominal / Equity)

### Why not use British/American classification of accounts?
Both classifications are more suited to business accounting. 

1. There is no need to record equity at the end of the period, it can be recalculated on the fly. The only accounts of `equity` type are  `Currency Trading` in all used currencies. They balance differences that occur due to multi-currency support according to current exchange rates and allow setting correct conversion on the date of transaction.
2. There is no need to differentiate between `Assets` and `Liabilities` because e.g. giving a loan to a person will create an `Asset` but getting a little more in return will be accounted as `Liability`. In business accounting netting documents are signed to compensate mutual liabilities, but we consider it overcomplicated for personal accounting and confusing to the user.
3. `Assets` respresent tangible monetary assets and `Loans` represent intangible assets or liabilities (recorded with a negative value). But both `Assets` and `Loans` can be a source/destination of monetary operations. So they are presented to user in the same scenarios.
4. `Income` and `Expense` account type are the only ones the exactly match classifications. They are valid to use in personal accounting as is.

## Types of entries
Entries are collections of transactions that represent user-friendly records.

Both `Assets` and `Loans` are available to the user as a source/destination of money operations.

There are 3 types of entries: income, expense, transfer.

> There is no need to storage entry type as it can be derived from account types used in the entry.

### Income

    Dr. Assets/Loans < Cr. Income

or

    Dr. Assets/Loans, EUR < Cr. Currency Trading, EUR
    Dr. Currency Trading, USD < Cr. Income, USD
    
### Expense

    Dr. Expense < Cr. Assets/Loans

or

    Dr. Expense, EUR < Cr. Currency Trading, EUR
    Dr. Currency Trading, USD < Cr. Assets/Loans, USD
        
### Transfer

    Dr. Assets/Loans < Cr. Assets/Loans

or

    Dr. Assets/Loans, EUR < Cr. Currency Trading, EUR
    Dr. Currency Trading, USD < Cr. Assets/Loans, USD

## Multiple currency support
The accounting system will not be biased towards one currency. All transactions will be recorded in the currencies they were actually carried out (source data). Though selection of base currency is necessary to calculate income/expense and net worth.

It is possible to change the base currency at any time. However it requires automatic recalculation of the all transactions with income or expense accounts.

Special accounts for each used currency are created with the name `Currency Trading` which balance currency conversions.

e.g. buying food with a different currency (EUR) from the base (USD)

    Dr. Currency Trading, EUR < Cr. Cash, EUR
    Dr. Food, USD < Cr. Currency Trading, USD
