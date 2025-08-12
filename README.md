# HW1: Bash & Git Warm-up

## Overview

This assignment helps you practice fundamental command-line skills and Git workflows that you'll use throughout the course. You'll write a bash script to automate a common data science task and demonstrate proper version control practices.

## Learning Objectives

By completing this assignment, you will:
- Write a functional bash script using command-line tools
- Practice Git fundamentals: initializing repos, staging, committing, and pushing
- Develop good version control habits with meaningful commit messages
- Automate a task that could be useful in computational social science research

## Instructions

### Step 1: Choose Your Scenario
Select **one** scenario from the `scenarios/` folder. Each scenario describes a task that a computational social scientist might need to automate. Read through all options and pick the one that interests you most.

Available scenarios:
- `scenario1_data_organization.md` - Organize messy research data files
- `scenario2_log_analysis.md` - Analyze web server logs for research
- `scenario3_text_preprocessing.md` - Prepare text files for analysis
- `scenario4_backup_automation.md` - Create automated backups of research files

### Step 2: Write Your Script
1. Create a file called `solution.sh` in the root directory
2. Make your script executable: `chmod +x solution.sh`
3. Your script should:
   - Include a clear header comment explaining what it does
   - Handle the specific task described in your chosen scenario
   - Include error checking where appropriate
   - Use meaningful variable names
   - Include comments explaining complex parts

### Step 3: Test Your Script
- Run your script multiple times to ensure it works correctly
- Test edge cases (empty directories, missing files, etc.)
- Make sure it produces the expected output

### Step 4: Document Your Work
1. Copy your chosen scenario file to the root directory as `chosen_scenario.md`
2. Create a file called `reflection.md` with:
   - Which scenario you chose and why
   - What challenges you encountered
   - How you tested your script
   - What you learned about bash scripting

### Step 5: Git Workflow
Throughout your work, practice good Git habits:

1. **Initial commit:**
   ```bash
   git add chosen_scenario.md
   git commit -m "Add chosen scenario for HW1"
   ```

2. **Incremental commits** as you develop:
   ```bash
   git add solution.sh
   git commit -m "Add initial script structure"
   
   git add solution.sh
   git commit -m "Implement main logic for [specific feature]"
   
   git add solution.sh
   git commit -m "Add error checking and comments"
   ```

3. **Final commit:**
   ```bash
   git add reflection.md
   git commit -m "Add reflection on bash scripting experience"
   ```

4. **Push your work:**
   ```bash
   git push origin main
   ```

## Deliverables

Your final repository should contain:
- `solution.sh` - Your bash script (executable)
- `chosen_scenario.md` - Copy of the scenario you chose
- `reflection.md` - Your reflection (300-500 words)
- **At least 3 meaningful Git commits** with descriptive messages

## Grading Rubric (15 points total)

| Component | Points | Criteria |
|-----------|--------|----------|
| **Script Functionality** | 7 pts | Script correctly solves the chosen scenario, handles errors gracefully, runs without issues |
| **Code Quality** | 3 pts | Clear comments, good variable names, organized structure, follows bash best practices |
| **Git Usage** | 3 pts | At least 3 commits with meaningful messages, proper repository organization |
| **Documentation** | 2 pts | Clear reflection demonstrating understanding, chosen scenario included |

## Tips for Success

**Bash Scripting:**
- Start simple and build complexity gradually
- Use `echo` statements to debug your script
- Test each part of your script separately before combining
- Remember: `$1`, `$2`, etc. are command-line arguments
- Use `if [ -f "filename" ]` to check if files exist

**Git Best Practices:**
- Commit early and often
- Write commit messages that explain *what* you changed and *why*
- Use `git status` frequently to see what's been modified
- Don't commit broken code - test before committing

**Getting Help:**
- Use `man command` to read documentation for bash commands
- Test commands in the terminal before putting them in your script
- Ask questions in bCourses discussion forum
- Attend office hours if you get stuck

## Submission

**GitHub:** Ensure all your work is pushed to this repository by the due date.

**bCourses:** Submit the URL of your GitHub repository and confirm you have at least 3 commits visible in the commit history.

## Academic Integrity

You may:
- Use online resources to learn bash syntax
- Discuss general approaches with classmates
- Ask for help debugging specific errors

You may not:
- Copy scripts from online sources
- Share your complete solution with classmates
- Submit work that is primarily written by someone else

If you use AI assistance (ChatGPT, Copilot, etc.), you must:
- Document this in your reflection
- Understand and be able to explain every line of your script
- Note: This is great practice for transparent AI use in research!