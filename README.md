# OrganizeMe - File Organization Tool

A Python tool to automatically organize files from an old hard drive (or any directory) by separating them into folders based on file types. Perfect for cleaning up messy directories and organizing large collections of files.

## Overview

**OrganizeMe** automatically scans a directory and moves files into categorized folders based on their file extensions. This makes it easy to organize files from old hard drives, downloads folders, or any directory with mixed file types.

## Project Structure

```
Python_Automation/
├── OrganizeMe/              # Main file organization tool
│   ├── organize.py         # The main file organization script
│   ├── AUDIO/              # Organized audio files
│   ├── DOCUMENTS/          # Organized document files
│   ├── IMAGES/             # Organized image files
│   ├── VIDEOS/             # Organized video files
│   ├── PHOTOSHOP/          # Organized Photoshop/SVG files
│   └── MISC/               # Miscellaneous unclassified files
└── examples/                # Example/test scripts (not part of main tool)
```

## Main Feature: File Organization

### How It Works

The `organize.py` script automatically:
- Scans all files in the current directory
- Categorizes files based on their file extension
- Creates category folders if they don't exist
- Moves files into their appropriate folders

### Supported File Types

- **DOCUMENTS**: `.pdf`, `.rtf`, `.txt`
- **AUDIO**: `.m4a`, `.m4b`, `.mp3`
- **VIDEOS**: `.mov`, `.avi`, `.mp4`
- **IMAGES**: `.jpg`, `.jpeg`, `.png`
- **PHOTOSHOP**: `.svg`
- **MISC**: Any other file types not in the above categories

### Usage

1. Copy `organize.py` to the directory containing files you want to organize
2. Run the script:
   ```bash
   python organize.py
   ```
3. Files will be automatically sorted into their respective folders

**Note**: The script organizes files in the directory where it's executed. Make sure to run it from the directory containing the files you want to organize.

## Installation

No external dependencies required! OrganizeMe uses only Python's built-in libraries:
- `os` - for directory operations
- `pathlib` - for path handling

Just make sure you have Python 3.6+ installed.

## Example: Organizing Files from an Old Hard Drive

1. Copy files from your hard drive to a directory (e.g., `~/old_harddrive_files/`)
2. Copy `organize.py` to that directory:
   ```bash
   cp Python_Automation/OrganizeMe/organize.py ~/old_harddrive_files/
   ```
3. Navigate to the directory and run the script:
   ```bash
   cd ~/old_harddrive_files/
   python organize.py
   ```
4. Files will be automatically sorted into:
   - `DOCUMENTS/` - PDFs, text files, RTF files
   - `AUDIO/` - Music and audio files
   - `VIDEOS/` - Video files
   - `IMAGES/` - Photos and images
   - `PHOTOSHOP/` - SVG files
   - `MISC/` - Everything else

## Important Notes

⚠️ **Warning**: The script will **move** files (not copy them). Make sure to:
- Back up important files before running
- Test on a small directory first
- Run from the correct directory

## File Location

- **Main script**: `Python_Automation/OrganizeMe/organize.py`

## Additional Examples

The `examples/` folder contains two showcase scripts that demonstrate additional automation capabilities:

- **`codementor.py`** - Complex Selenium automation example showing:
  - Multi-step workflow automation (login → add to cart → checkout)
  - Proper use of WebDriverWait and expected conditions
  - Environment variable usage for secure credential handling
  - Form automation with dropdowns and text inputs

- **`scrapePages.py`** - Web scraping example demonstrating:
  - BeautifulSoup for HTML parsing
  - Pagination handling across multiple pages
  - Data extraction and parsing techniques

These examples showcase web automation and scraping skills beyond the main file organization tool.

## Future Improvements

Potential enhancements:
- Add option to copy instead of move files
- Add progress indicators for large file operations
- Support for more file types
- Recursive directory scanning
- Duplicate file detection
- File size reporting
- Custom category configuration

