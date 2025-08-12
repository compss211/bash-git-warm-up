# Scenario 3: Text Data Preprocessing Pipeline

## The Problem

You've collected thousands of social media posts, news articles, and survey responses for your research on public opinion about climate change. Before you can analyze this text data, it needs to be cleaned and standardized. Different sources have different formats, encodings, and quality issues.

## Your Task

Create a bash script that preprocesses text files to prepare them for computational analysis (NLP, sentiment analysis, etc.).

## Sample Input Data
You have text files with various issues:
```
raw_text/
├── twitter_posts.txt          # Contains @mentions, #hashtags, URLs
├── news_articles.txt          # Has HTML tags, extra whitespace
├── survey_responses.txt       # Mixed encodings, inconsistent formatting
├── reddit_comments.txt        # Has [deleted] and [removed] entries
└── facebook_posts.txt         # Contains emojis, special characters
```

## Requirements

Your script should create a preprocessing pipeline that:

1. **Text Cleaning:**
   - Remove URLs (http://, https://, www.)
   - Remove HTML tags (< and >)
   - Remove email addresses
   - Clean up extra whitespace (multiple spaces, tabs, empty lines)
   - Remove or flag deleted/removed content markers

2. **Format Standardization:**
   - Convert all text to lowercase (optional flag)
   - Remove or replace special characters based on needs
   - Standardize line endings (Unix format)
   - Handle different text encodings

3. **Social Media Specific:**
   - Extract hashtags to separate file (for analysis)
   - Extract @mentions to separate file
   - Count and report social media elements removed

4. **Quality Control:**
   - Remove entries shorter than N words (configurable)
   - Flag potential spam/bot content (repeated phrases)
   - Create summary statistics of cleaning process

## Sample Output Structure
```
processed_text/
├── cleaned/
│   ├── twitter_posts_clean.txt
│   ├── news_articles_clean.txt
│   ├── survey_responses_clean.txt
│   ├── reddit_comments_clean.txt
│   └── facebook_posts_clean.txt
├── extracted/
│   ├── hashtags.txt
│   ├── mentions.txt
│   └── urls.txt
├── stats/
│   └── preprocessing_report.txt
└── README.md
```

## Sample Report Output
```
=== TEXT PREPROCESSING REPORT ===
Date: 2024-01-15
Input Files: 5
Total Input Lines: 12,487

CLEANING STATISTICS:
- URLs removed: 1,234
- HTML tags removed: 456
- Empty lines removed: 890
- Short entries removed: 234 (< 3 words)

SOCIAL MEDIA ELEMENTS:
- Hashtags extracted: 567
- @mentions extracted: 345
- Top hashtags: #climatechange (45), #globalwarming (32)

OUTPUT:
- Clean text files: 5
- Total output lines: 10,123
- Average words per entry: 15.6
- Data reduction: 18.9%
```

## Test Your Script

Create sample text files with various formatting issues to test your preprocessing pipeline.

## Script Requirements

- Accept input directory as command-line argument
- Allow optional flags (e.g., `--lowercase`, `--min-words=5`)
- Provide progress feedback during processing
- Generate comprehensive report

## Bonus Challenge (Optional)

- Add language detection (filter non-English text)
- Implement basic spam detection
- Add option to preserve original files vs. overwrite
- Create configuration file for preprocessing options

## Real-World Application

Text preprocessing is essential in computational social science for analyzing social media data, survey responses, news content, and other textual sources. Clean, standardized text improves the quality of downstream analysis like sentiment analysis, topic modeling, and content classification.