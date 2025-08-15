# Budget Data
A data structure specification for budget apps

## A Note about IDs

The IDs for each object (e.g. an Account ID) can be any non-empty identifier
unique to that list of objects (e.g. Accounts). You can use UUIDs, but that is
not required.

You are also free to use `_id` rather than `id` as the name of each of the ID
fields, AS LONG AS IT IS CLEAR which you are using (i.e. don't have both an `id`
field and an `_id` field). However, foreign-key fields (such as `accountId`)
must use the names documented below (i.e. do not use `account_id`).

## Specification

### Accounts

The list of a user's financial accounts:

    [
      {
        "name": "*account name*",
        "id": "*account id*"
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
        "id": "*category id*"
      },
      *...*
    ]

### Transactions

    [
      {
        "id": "*transaction id*",
        "accountId": "*account id*",
        "amountTotal": *transaction total, in cents*,
        "categoryAmounts": {
          "*category id*": *amount from this category, in cents*,
          *...*
        },
        "note": "*optional textual comment about this transaction*",
        "timestamp": *date/time of transaction, as a JavaScript unix timestamp*,
        "who": "*name of payee*"
      },
      *...*
    ]
