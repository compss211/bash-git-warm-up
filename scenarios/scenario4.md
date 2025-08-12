# Scenario 4: Automated Research Data Backup

## The Problem

You're working on a long-term computational social science project with valuable data, code, and analysis results. You need an automated backup system to protect against data loss, but manual backups are time-consuming and easily forgotten. Different types of files need different backup frequencies.

## Your Task

Create a bash script that automatically backs up research files with smart scheduling and organization.

## Sample Research Directory Structure
```
research_project/
├── data/
│   ├── raw/                    # Original data (backup daily)
│   ├── processed/              # Cleaned data (backup daily) 
│   └── archives/               # Old versions (backup weekly)
├── code/
│   ├── analysis/               # Analysis scripts (backup daily)
│   ├── scraping/              # Data collection (backup daily)
│   └── experiments/           # Test code (backup weekly)
├── results/
│   ├── figures/               # Plots, charts (backup daily)
│   ├── tables/                # Statistical output (backup daily)
│   └── drafts/                # Paper drafts (backup immediately)
├── documentation/
│   ├── notes/                 # Research notes (backup daily)
│   └── references/            # Papers, citations (backup weekly)
└── temp/                      # Temporary files (never backup)
```

## Requirements

Your script should:

1. **Smart File Selection:**
   - Backup only files changed since last backup
   - Skip temporary files and common junk (.DS_Store, .tmp, .cache)
   - Handle different backup frequencies by directory
   - Detect and backup critical files immediately (.py, .R, .do, .txt)

2. **Organized Backup Structure:**
   ```
   backups/
   ├── daily/
   │   └── 2024-01-15/
   │       ├── data/
   │       ├── code/
   │       └── results/
   ├── weekly/
   │   └── 2024-week-03/
   └── emergency/
       └── immediate_backup_20240115_143022/
   ```

3. **Backup Management:**
   - Create timestamped backup directories
   - Compress older backups to save space
   - Remove backups older than N days (configurable)
   - Maintain multiple backup generations

4. **Safety and Verification:**
   - Verify backup integrity (file sizes, checksums)
   - Never overwrite existing backups
   - Log all backup activities with timestamps
   - Provide detailed backup reports

## Sample Output/Report
```
=== RESEARCH BACKUP REPORT ===
Backup Date: 2024-01-15 14:30:22
Backup Type: Daily
Target Directory: /path/to/research_project

FILES PROCESSED:
- New files backed up: 23
- Modified files backed up: 7
- Files skipped (no changes): 145
- Files ignored (temp/cache): 12

BACKUP STATISTICS:
- Total backup size: 2.3 GB
- Compression ratio: 65%
- Backup duration: 45 seconds
- Verification: PASSED

DIRECTORY BREAKDOWN:
- data/: 15 files (1.2 GB)
- code/: 8 files (45 MB)
- results/: 5 files (890 MB)
- documentation/: 2 files (12 MB)

BACKUP MANAGEMENT:
- Current backup location: backups/daily/2024-01-15/
- Previous backup: 2024-01-14 (retained)
- Old backups cleaned: 2 (older than 30 days)
- Available disk space: 78%

STATUS: SUCCESS ✓
```

## Script Features

Your backup script should support:

```bash
# Basic usage
./backup_research.sh

# With options
./backup_research.sh --type=weekly --verbose --compress
./backup_research.sh --emergency --no-compress
./backup_research.sh --clean-old --dry-run
```

## Command-line Options
- `--type=daily|weekly|emergency` - Backup type
- `--verbose` - Detailed output during backup
- `--compress` - Compress backup files
- `--clean-old` - Remove old backups
- `--dry-run` - Show what would be backed up without doing it
- `--config=file` - Use custom configuration file

## Test Your Script

Create a mock research directory with various file types and test your backup script with different scenarios.

## Bonus Challenge (Optional)

- Add email notifications when backups complete/fail
- Implement incremental backups (only store changes)
- Add support for remote backup destinations
- Create a restore function to recover from backups
- Add backup scheduling integration (cron job setup)

## Real-World Application

Automated backups are crucial for research data management and reproducibility. Many computational social science projects involve months or years of data collection and analysis that would be devastating to lose. This type of automation ensures consistent data protection without relying on human memory.