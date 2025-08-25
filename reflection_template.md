# README.md Template

Use this template for your README.md file:

---

# HW1: [Your Chosen Scenario]

**Name:** [Your Name]  
**Scenario:** Option [1/2/3] - [File Organizer/Batch Renamer/Log Cleaner]

## What My Script Does

[Explain in 1-2 sentences what your script accomplishes]

## How to Run It

```bash
# Command to run your script
./your_script_name.sh
```

## Why I Chose This Scenario

[1-2 sentences about why you picked this option]

## Bash Commands I Used

- `command1` - what it does
- `command2` - what it does
- etc.

## What I Learned

[2-3 sentences about what you learned from this assignment]

## Testing

[Briefly describe how you tested your script]

---

**Example README.md:**

# HW1: File Organizer

**Name:** Jane Student  
**Scenario:** Option 1 - File Organizer

## What My Script Does

My script automatically sorts files into three folders (images, documents, archives) based on their file extensions.

## How to Run It

```bash
./organize_files.sh
```

## Why I Chose This Scenario

I chose the file organizer because I often have messy download folders and wanted to learn how to automate cleaning them up.

## Bash Commands I Used

- `mkdir -p` - creates directories if they don't exist
- `mv` - moves files to different locations  
- `echo` - prints status messages
- `2>/dev/null` - hides error messages for missing files

## What I Learned

I learned how wildcards work in bash (like *.jpg) and how to redirect error output. The most challenging part was handling cases where no files of a certain type exist.

## Testing

I created sample files with different extensions and ran the script multiple times to make sure it worked correctly and didn't crash when no files were found.