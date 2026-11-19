# odt_test_addons

Test repository for the Module Registry **Download Modules** button and its
docs and tests scan. These are not installable Odoo modules.

| Folder | What it tests |
| --- | --- |
| 7 `odt_*` folders at the root | Normal modules: name, version, license, author, depends |
| `odt_project_timesheet` | Version `1.0`: Odoo version comes from the branch name only |
| `addons_extra/odt_pos_receipt` | Module in a sub-folder |
| `odt_broken_manifest` | Not a plain dict: must be skipped |

Expected on a branch named `19.0`: 9 modules added, 1 skipped.

## Scan (README.md and tests/test_*.py in the module folder)

| Module | Description | README | Tests | Expected scan |
| --- | --- | --- | --- | --- |
| `odt_account_check` | yes | yes | yes | Success |
| `odt_purchase_approval` | yes | yes | yes | Success |
| `addons_extra/odt_pos_receipt` | yes | yes | yes | Success (sub-folder) |
| `odt_crm_lead_score` | yes | yes | no | Failed: no tests |
| `odt_sale_discount` | no | yes | no | Failed: no tests |
| `odt_hr_attendance_report` | yes | no | yes | Failed: no README |
| `odt_stock_barcode_label` | no | no | yes | Failed: no README |
| `odt_website_contact` | no | yes | only `tests/__init__.py` | Failed: no tests |
| `odt_project_timesheet` | no | no | no | Failed: both missing |

This README at the repository root does not count for any module.
