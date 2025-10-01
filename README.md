# File-Integrity-Checker
This Python project monitors files in a directory, detects modifications or missing files using SHA-256 hashes, creates backups of changed files, and produces timestamped CSV reports.

## What is File-Integrity-Checker
File integrity checkers are tools designed to monitor and verify that files on a system have not been tampered with. They work by generating cryptographic one-way hashes, such as SHA-256, for each file. A cryptographic one-way hash is a mathematical function that converts a file’s content into a fixed-length unique value, or “fingerprint,” in such a way that even a small change in the file will produce a completely different hash. These hashes are stored in a baseline dataset (like a JSON file in this project), and comparing current hashes to the stored baseline allows the tool to detect modified, missing, or tampered files.

Cryptographic one-way hashes provide a reliable way to ensure file integrity because the original file cannot be reconstructed from its hash. This makes it practically impossible for an attacker to alter a file without being detected. In addition to monitoring changes, file integrity checkers can create backups of altered files, generate timestamped CSV reports, and facilitate restoring files to their previous state, which is benefecial to protect critical files and maintain system security.

## Features
- Build a database of SHA-256 hashes for files
- Detect modified, missing, or tampered files
- Backup modified files while preserving directory structure
- Generate timestamped CSV reports
- Restore files to previous state from backup


## How To Run

Create a directory containing the files you want to check.

Note the path to this folder for later use in the script and run the Python script. By choosing :

1 – Build database: Generates a baseline dataset of SHA-256 hashes for all files in the folder. Run this first to initialize the monitoring database.

2 – Check integrity: Compares current file hashes with the database. If changes are detected, you can optionally specify a backup folder and a CSV report path to save modified files and logs.

3 – Restore files: You are able to restore files from a backup directory that were saved during the integrity check in stage 2.

## Dependencies
- Python 3.x
-  Python libraries:
    - hashlib
    - os
    - json
    - shutil
    - csv
    - datetime



## Contact
 Project by: Nazanin Mahmoudy, 2025                      
 Email: Nazaninmahmoudy@gmail.com                      
 GitHub: https://github.com/Nazaninmahmoudi                                
 Kaggle: https://www.kaggle.com/nazaninmahmoudy 
