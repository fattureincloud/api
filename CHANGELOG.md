# Changelog

All notable changes to this project will be documented in this file.
* Major versions are made in case of big changes that create notable breaking changes in one or more methods.
* Minor versions are made in case of notable changes, new methods added, or small breaking changes made to prevent subsequent problems upstream.
* Patch versions for all other small changes or fixes.

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
* **Transform Issued Documents**: added endpoint transform issued documents.
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

## 2.1.0 (2022-08-12)

### Changed

* **Create Issued Document**: *ei_data.od_number* and *oei_data.d_date* parameters are now required when *ei_data.original_document_type* is specified.
* **Create Issued Document**: *ei_data.payment_method* parameter is now required when *e_invoice* is set to true.

### Fixed

* fixed issue causing a 500 error in case of *fields* parameter set as empty string in LIST and GET methods
