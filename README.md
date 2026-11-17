# odt_test_addons

Test repository for the Module Registry **Download Modules** button.
Each folder holds only a `__manifest__.py`; these are not installable Odoo modules.

| Folder | What it tests |
| --- | --- |
| 7 `odt_*` folders at the root | Normal modules: name, version, license, author, depends |
| `odt_project_timesheet` | Version `1.0`: Odoo version comes from the branch name only |
| `addons_extra/odt_pos_receipt` | Module in a sub-folder |
| `odt_broken_manifest` | Not a plain dict: must be skipped |

Expected on a branch named `19.0`: 9 modules added, 1 skipped.
