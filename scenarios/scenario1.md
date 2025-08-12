# Scenario 1: Research Data Organization

## The Problem

You're working with a research team studying social media behavior. Over several months, different team members have collected data files with inconsistent naming conventions. The files are scattered in a single directory and need to be organized for analysis.

## Your Task

Write a bash script that organizes research data files into a proper directory structure.

## Sample Data Structure (Before)
```
data_directory/
├── tweets_jan_2024.csv
├── FACEBOOK_posts_january.json
├── reddit-comments-jan-24.txt
├── tweets_feb_2024.csv
├── Instagram_Feb_2024.csv
├── facebook_posts_february.json
├── Reddit_Comments_Feb_2024.txt
├── tweets_march_2024.csv
├── insta_march.csv
├── README.txt
└── analysis_notes.md
```

## Requirements

Your script should:

1. **Create organized directories** by platform and month:
   ```
   organized_data/
   ├── twitter/
   │   ├── january/
   │   ├── february/
   │   └── march/
   ├── facebook/
   ├── reddit/
   ├── instagram/
   └── documentation/
   ```

2. **Move files** to appropriate directories based on:
   - Platform name (twitter, facebook, reddit, instagram)
   - Month mentioned in filename
   - File type (.csv, .json, .txt)

3. **Handle edge cases:**
   - Files that don't match any platform (move to `other/`)
   - Documentation files (README, notes) go to `documentation/`
   - Don't overwrite existing files (add timestamp if needed)

4. **Provide feedback:**
   - Print which files are being moved where
   - Count how many files were organized
   - Report any files that couldn't be categorized

## Test Your Script

Create a test directory with sample files (you can create empty files with `touch filename.csv`) and run your script to verify it works correctly.

## Bonus Challenge (Optional)

- Add a flag to preview moves without actually moving files (`-n` or `--dry-run`)
- Standardize filenames while moving (e.g., convert "FACEBOOK_posts_january.json" to "facebook_posts_january.json")

## Real-World Application

This type of data organization is common in computational social science research where multiple researchers contribute data over time. Good file organization makes analysis more efficient and reproducible.