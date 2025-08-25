# HW1: Bash & Git Warm-Up

## Overview

This assignment helps you practice using **basic Bash commands** and **Git version control** by scripting a simple automation task and tracking your work with Git commits.

---

## Getting Started

1. **Clone your repository** to your local machine:
   ```bash
   git clone [your-repo-url]
   cd hw1-bash-git-warmup-yourusername
   ```
2. **Choose one scenario** below and start coding!

---

## 📌 Scenarios (Choose ONE)

Pick **one** scenario below based on your current comfort level with bash and git:

### Path A — Beginner: File Organizer (organize_files.sh)
Write a script called `organize_files.sh` that:
- Creates folders called `images/`, `documents/`, and `archives/`
- Moves all `.jpg`, `.png` files into `images/`
- Moves `.pdf` and `.docx` files into `documents/`
- Moves `.zip`, `.tar.gz` files into `archives/`
- Prints a message showing how many files were moved

Use: mkdir -p, mv, echo, ls/globs, wc -l

### Path B — Intermediate: Log Cleaner (clean_logs.sh)
Write a script called clean_logs.sh that:
- Creates a cleaned_logs/ directory
- Copies all .log files to the new directory
- Removes any lines containing “ERROR” or “WARN” from the copied files (case-insensitive)
- Reports how many lines were removed in total across all files

Use: a loop, grep -viE, wc -l, mkdir -p, cp

### Path C — Advanced: CSV Combiner (combine_csv.sh)
Write a script called combine_csv.sh that:
- Creates a combined/ directory
- Finds all .csv files in the current folder
- Appends them into a single file called combined/all.csv
- Removes duplicate lines from all.csv and saves the clean version as all_dedup.csv
- Prints how many rows were in the combined file and how many remain after deduplication

Use: mkdir -p, cat, sort -u, wc -l, loops or for f in *.csv


---

## What Your Repository Should Contain

When you're finished, your repository should have:

### 1. Your Bash Script
- Choose one scenario and create the corresponding script
- Make it executable with `chmod +x script_name.sh`
- Include comments explaining what each part does
- Test it to make sure it works!

### 2. A README.md File (replace this file)
Create a new README.md that includes:
- **What your script does** (1-2 sentences)
- **How to run it** (the exact command)
- **What scenario you chose and why**
- **What bash commands you used** (mkdir, mv, cp, etc.)
- **What you learned**

### 3. Git Commit History
Your repository should show **at least 3 commits** with good commit messages:
- Initial commit (update README with your scenario choice)
- Add script draft
- Final working version

### 4. Test Files (optional)
If you created test files to check your script, you can include them in a `test_files/` directory

---

## Bash Commands You Might Need

| Command | What it does | Example |
|---------|--------------|---------|
| `mkdir -p dirname` | Create directory | `mkdir -p images/` |
| `mv file destination/` | Move file | `mv *.jpg images/` |
| `cp file destination/` | Copy file | `cp *.log cleaned_logs/` |
| `find . -name "*.txt"` | Find files | `find . -name "*.log"` |
| `grep -v "ERROR"` | Remove lines with "ERROR" | `grep -v "ERROR" file.log` |
| `echo "message"` | Print message | `echo "Files organized!"` |
| `read -p "prompt" var` | Get user input | `read -p "Enter prefix: " prefix` |

---

## Git Workflow 

```bash
# Check status and add your work
git status
git add script_name.sh
git commit -m "Add initial script for [scenario name]"

# Make improvements and commit again
git add script_name.sh
git commit -m "Fix bug in file detection logic"

# Update your README
git add README.md
git commit -m "Update README with script documentation"

# Push your changes to GitHub
git push origin main

# Check your commit history
git log --oneline
```

---

## Things to Focus On

| Component | What we're looking for |
|-----------|------------------------|
| **Script Works** | Script runs without errors and completes the chosen scenario |
| **Code Quality** | Clean code with comments, good variable names |
| **Git Usage** | At least 3 commits with meaningful messages, proper workflow |
| **Documentation** | Clear README explaining what the script does and how to use it |

---

## Tips for Success

- **Start simple!** Get basic functionality working first
- **Test frequently** - run your script on sample files
- **Use `echo` statements** to debug and show progress
- **Commit early and often** - don't wait until the end
- **Read error messages** - they usually tell you what's wrong
- **Push your changes regularly** so your work is saved on GitHub

---

## FAQ

**Q: Can't I just have ChatGPT write my script?**  
You *can* certainly ask ChatGPT (or Copilot, or any LLM) to write a Bash script — but that’s not the point of this assignment. The real learning goal is to understand what the script is doing, why certain commands are used, and how to debug when things break. If you just copy–paste an AI’s answer, you’ll:
- Miss the practice with basic Bash syntax you’ll need later in the course.
- Be unable to explain or adapt the code when it doesn’t quite fit your use case.
- Risk introducing subtle bugs (LLMs often hallucinate flags or commands that don’t exist).

That said, you can use AI as a helper if you do it transparently:
- Ask it for reminders of syntax (How do I move all .jpg files into a folder with Bash?).
- Compare your own code against its suggestions.
- Document your usage in a comment (e.g., # Used ChatGPT to suggest grep syntax; tested and modified).

In short: don’t outsource the whole script. Use AI like a reference or tutor — not as a substitute for your own thinking. You’ll get full credit for trying, documenting, and learning, even if your script isn’t perfect.

**Q: Which online resources can I use to learn bash commands?**  
A: Use `man` pages, LLM information, Stack Overflow, and bash tutorials.

**Q: What if my script doesn't work perfectly?**  
A: That's okay! We're grading on effort and learning. Document what you tried in your README.

**Q: How do I make my script executable?**  
A: Run `chmod +x your_script.sh` before testing it.

**Q: I'm getting "permission denied" when running my script**  
A: Make sure you made it executable and run it with `./script_name.sh`

**Q: Should I commit test files?**  
A: You can include them in a `test_files/` folder if you want, but it's not required.