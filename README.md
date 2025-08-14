# Budget Data
A data structure specification for budget apps

## Specification

### Accounts

The list of a user's financial accounts:

    [
      {
        "name": "*account name*",
        "uuid": "*account uuid*"
      },
      *...*
    ]

### Categories

A user's list of budget categories, including the amount currently budgeted (per
month) for each category:

    [
      {
        "budgeted": *allotted amount per month for this category, in cents*,
        "name": "*category name*",
        "remaining": *amount remaining in this category*,
        "refilled": "*YYYY-MM*"
        "uuid": "*category uuid*"
      },
      *...*
    ]

### Transactions

    [
      {
        "uuid": "*transaction uuid*",
        "accountUuid": "*account uuid*",
        "amountTotal": *transaction total, in cents*,
        "categoryAmounts": {
          "*category uuid*": *amount from this category, in cents*,
          *...*
        },
        "note": "*optional textual comment about this transaction*",
        "timestamp": *date/time of transaction, as a JavaScript unix timestamp*,
        "who": "*name of payee*"
      },
      *...*
    ]
