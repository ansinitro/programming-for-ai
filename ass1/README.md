# Assignment 1 — Working with Directories and Files in Python  

## 📝 Task 1 (25 points) — Working with Folders and Files

### 1. Creating Project Structure
Write a Python script that creates the following project directory:
```

project/
│
├── data/
└── results/

```

### 2. Working with CSV Files
- In the `data` folder, create a file `students.csv` containing students’ data:
  - Full name  
  - Group  
  - Grades  
- Read the file and calculate the **average score** for each student.

### 3. Save Results
- Save aggregated results in JSON format:  
  `results/report.json`
- If the file already exists — show a **warning** and ask for confirmation before overwriting.

### 4. Archiving
- Automatically create an archive `results.zip` that includes the `results` folder.

### 5. Working with `pathlib`
- Implement a check to see if `report.json` exists.  
  If it does, print its **file size** and **last modification date**.

---

## 📝 Task 2 (25 points) — Search for a Word in Text Files

- Generate **5 text files** (e.g., `name_1.txt`, `name_2.txt`, …) in one folder.  
- Each file contains arbitrary text.  
- Write a program that:
  - Accepts a **search query** (single word or phrase).
  - Outputs the **names of files** that contain the substring.
  - If no matches found — display an appropriate message.

**Input example:**
```

probability theory

```

**Output example:**
```

Found in: file2.txt, file4.txt

```

---

## 📝 Task 3 (25 points) — File Information

Given a text file `file.txt`, write a program that outputs:

- Number of Latin letters  
- Number of words  
- Number of lines  

---

## 📝 Task 4 (25 points) — Replacing Forbidden Words

Files provided:
- `words.txt`
- `forbidden_words.txt`

In `forbidden_words.txt`, forbidden words are separated by spaces.

Write a program that:
- Replaces **all forbidden words** in `words.txt` with `*` (asterisks).
- The number of `*` equals the number of letters in the forbidden word.
- Replacement is **case-insensitive** and applies even inside other words.

**Example:**
If `exam` is forbidden, then:
```

exam, Exam, EXAM → ****

```

**Output format:**  
Edited text according to the task condition.

---

## 🧩 Questions for Self-Monitoring

1. How can I open a file for reading and writing in Python?  
2. What is the difference between the file modes `'r'`, `'w'`, `'a'`, `'rb'`, `'wb'`?  
3. What is the advantage of using `with open(...) as f:`?  
4. How to close a file correctly and why is it important?  
5. What are the main functions of the `os` module for directories?  
6. How to create or delete folders in Python?  
7. What is the difference between `os.getcwd()` and `os.chdir()`?  
8. How to list files and folders in a directory?  
9. What is the `os.path` module used for?  
10. How to check if a file or folder exists?  
11. Why is `pathlib` more convenient than `os.path`?  
12. How to combine file paths cross-platform?  
13. How to read a CSV file in Python?  
14. Why use the `csv` module instead of line-by-line reading?  
15. How to serialize Python data into JSON?  
16. What is the difference between JSON and CSV?  
17. What Python data types can be stored in JSON?  
18. What is lazy loading and why is it used?  
19. How to read a large file line-by-line?  
20. What does `readline()` do? How to iterate over file objects?  
21. When should you use generators for files?  
22. What modules can handle archives (`.zip`, `.tar`)?  
23. How to create a `.zip` archive in Python?  
24. How to unzip an archive into a specific folder?  
25. What are the features of working with binary files (`.png`, `.exe`)?  

---

### 💡 Recommended Python Modules
- `os`
- `pathlib`
- `csv`
- `json`
- `zipfile`
