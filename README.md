# FileOrganizer — Python file sorting utility

A small command-line tool for organising files into category folders based on filename extension.

**This copy is an adaptation or redistributable copy of third-party source code**, with an [MIT licence crediting EnricoDevCpp](LICENSE). Please respect the original author; this repository is not presented as a newly authored utility by sacuar.

## What it does

- Walks a chosen directory recursively and moves files into category folders.
- Categories: Videos, Music, Images, Documents, Archives, Executables, Scripts and Others.
- Avoids overwriting files of the same name by adding a numeric suffix.
- Prints a summary at the end.

**Caution:** Files are actually **moved**, not copied. There is no dry-run, undo or backup feature in this version. Do not run it on your entire home folder, system folders, or directories containing important files without taking a backup. First test on an expendable folder.

## Run from source

Requires Python 3, no third-party Python packages.

```bash
git clone https://github.com/sacuar/FileOrganizer.git
cd FileOrganizer
python FileOrganizer.py group "/path/to/a/test-folder"
```

On Windows, a sample path might be:

```powershell
py FileOrganizer.py group "C:\Users\Public\Documents\OrganizerTest"
```

**Important:** This is a Python script, not a Python package and not a command that executes a remote ZIP file. You should inspect `FileOrganizer.py` before running it.

## Improvements and contributions

Contributor help is welcome for useful safeguards:

- A **dry-run / preview mode** before moving files.
- Optional recursion and custom category mappings.
- Safer handling of symlinks, permissions and name collisions.
- Automated tests that use temporary directories.
- A restore log or undo support.

[Open an issue](https://github.com/sacuar/FileOrganizer/issues) or propose a focused pull request. Avoid including your personal files in test data.

## Attribution and licensing

The included [MIT License](LICENSE) credits **EnricoDevCpp (2026)**. The Python source contains the original author's optional support URL. Those attribution and licence terms are retained. The previous README contained unrelated and misleading external download links, which have been removed.

Source code: [FileOrganizer.py](FileOrganizer.py).
