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

### Budget

The amount a user has currently budgeted (per month) for each category:

    {
      "*category uuid*": {
        "budgeted": *allotted amount for this month, in cents*,
        "remaining": *amount remaining in this category*,
        "refilled": "*YYYY-MM*"
      },
      *...*
    }

### Categories

A user's list of budget categories:

    [
      {
        "name": "*category name*",
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
