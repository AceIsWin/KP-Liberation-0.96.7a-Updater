# Liberation Upgrade Script (0.96.7a → 0.96.8)

This Python script automates the process of updating classnames in a Liberation mission from version **0.96.7a** to **0.96.8l**. It scans and modifies relevant files, replacing outdated classnames with their newer counterparts.

## ⚠️ Manual Adjustments Required
The script does **not** automatically update:
- `"KPLIB_b_objectsDeco"` → `"buildings"` *(This is too broad and may cause unintended replacements.)*
- `"KPLIB_c_units"` → `"civilians"` *(This can match unintended strings.)*

These changes need to be handled **manually** after running the script.

## Features
✅ Recursively scans and updates all files in a given directory  
✅ Creates backups (`.bak` files) before modifying any files  
✅ Supports filtering by file extension (e.g., `.sqf`, `.hpp`, `.cfg`)  
✅ Dry-run mode to preview changes before applying them  

## Usage

```sh
python classname_updater.py <directory> --extensions sqf hpp cfg --dry-run
