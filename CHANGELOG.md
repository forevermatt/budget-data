# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [3.0.0] - 2026-10-01
### Changed
- Omit a transaction's `accountId` when it is not tied to an account

### Added
- Define negative transaction amounts as money put into a category

### Fixed
- Add the missing comma after a category's `refilled` field
- Say that a category's `remaining` amount is in cents

## [2.1.0] - 2026-09-18
### Added
- Add "Recurring Transactions" record type specification

### Fixed
- Use JSON syntax highlighting for record-type specifications

## [2.0.0] - 2025-08-15
### Removed
- Remove `budget` data as a separate list

### Changed
- Merge `budget` data fields into `categories` data
- Rename `uuid` fields to `id` (or optionally `_id`)

## [1.1.0] - 2020-12-03
### Added
- Add a "note" field to `transactions`

## [1.0.0] - 2020-07-12
### Added
- Specify structure of `accounts` data
- Specify structure of `budget` data
- Specify structure of `categories` data
- Specify structure of `transactions` data

[Unreleased]: https://github.com/forevermatt/budget-data/compare/3.0.0...develop
[3.0.0]: https://github.com/forevermatt/budget-data/releases/tag/3.0.0
[2.1.0]: https://github.com/forevermatt/budget-data/releases/tag/2.1.0
[2.0.0]: https://github.com/forevermatt/budget-data/releases/tag/2.0.0
[1.1.0]: https://github.com/forevermatt/budget-data/releases/tag/1.1.0
[1.0.0]: https://github.com/forevermatt/budget-data/releases/tag/1.0.0
