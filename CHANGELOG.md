# Changelog

All notable changes to this project will be documented in this file.
* Major versions are made in case of big changes that create notable breaking changes in one or more methods.
* Minor versions are made in case of notable changes, new methods added, or small breaking changes made to prevent subsequent problems upstream.
* Patch versions for all other small changes or fixes.

* ## 2.6.1 (2024-05-27)

### Changed

* **Company**: added *vat_number* field.
* **IssuedDocument**: removed *show_paypal_button* field.
* **IssuedDocumentExtraData**: removed *show_sofort_button* field.

### Added

* **Filters**: added *not like* and *not contains* filters.

## 2.6.0 (2024-03-06)

### Changed

* **Company**: added *fic_plan* and *fic_license_expire* fields.

### Added

* **Get Company Plan Usage**: added endpoint to get plan resources limits usage.

## 2.5.2 (2023-10-09)

### Changed

* **Client - Supplier**: added *contry_iso* field.
* **Issued/Received Document**: added *locked* field.

### Added

* **Create Webhooks Subscription**: added *config.mapping* field to receive webhooks data in the request body.

## 2.5.1 (2023-02-27)

### Added

* **Send EInvoice Dry Run**: added the *options.dry_run* field to the Send EInvoice method for testing purposes.

### Changed

* **Create Entity**: create Client/Supplier now returns a specific error about the reason of the conflict.

### Fixed

* **Issued/Received Documents updated_at**: *updated_at* field now is updated also when the document is set as paid from Fatture in Cloud web.

## 2.5.0 (2023-01-30)

### Changed

* **Monthly quotas**: monthly quotas are now incremented from 20k to 40k per month.

### Fixed

* **Country iso**: Canary Islands country iso is now *IC* so it does not interfere anymore with *ES* (Spain).

## 2.4.0 (2023-01-05)

### Changed

* **Lists validations**: *Issued Documents*, *Received Documents* and *Receipts* now are subjected to stronger validations regarding the *items_list* and *payments_list* fields.
* **Dates validations**: all fields that are supposed to contain a date can no more contain invalid values.

## 2.3.0 (2022-11-29)

### Changed

* **Attachments**: all attachments related urls are now temporary.
* **Create Issued Document**: added *entity.id* validations (if it does not exist a 422 error is returned).

## 2.2.0 (2022-11-21)

### Added

* **List Emails**: added endpoint to list sent emails.
* **Transform Issued Documents**: added endpoint to transform issued documents.
* **Join Issued Documents**: added endpoint to join issued documents.

### Changed

* **Issued Document**: added *created_at* and *updated_at* fields.
* **Entity**: added *country_iso* field.

* Attachment urls are now temporary, every type of document and resource is effected.

### Fixed

* fixed invalid API request json body returned error.

## 2.1.1 (2022-09-15)

### Changed

* monthly private apps limits are now added up togheter for a maximum of 20000 calls per month per company, public apps limits remain unchanged at 20000 calls per month per company for each app.
