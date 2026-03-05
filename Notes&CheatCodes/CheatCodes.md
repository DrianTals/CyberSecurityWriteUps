# Cheat Codes

## Burp Suite Cheat Codes
## 🔹 Important Tabs
## 1️⃣ Proxy

- Intercepts browser requests

- Turn Intercept ON

- Modify requests before sending

## 2️⃣ Target

- View site structure

- Analyze URLs & parameters

## 3️⃣ Repeater

- Send request multiple times

- Modify parameters manually

- Great for testing SQLi, XSS

## 4️⃣ Intruder

- Automate attacks (brute force, fuzzing)

- Positions → Select payload location

- Payloads → Add wordlist

- Start attack

🔹 Basic Burp Workflow

- Set browser proxy to 127.0.0.1:8080

- Turn Intercept ON

- Capture request

- Send to Repeater / Intruder

- Analyze response

## Kali Linux Cheat Codes
- **Navigaton**
    - pwd            # Show current directory
    - ls             # List files
    - ls -la         # List all files (including hidden)
    - cd folder      # Enter folder
    - cd ..          # Go back one directory
    - cd /           # Go to root
- **File & Folder Management**
    - mkdir test     # Create folder
    - rmdir test     # Remove empty folder
    - rm file.txt    # Delete file
    - rm -rf folder  # Delete folder (force)
    - cp a.txt b.txt # Copy file
    - mv a.txt b.txt # Move or rename file
- **Viewing Files**
    - cat file.txt
    - less file.txt
    - head file.txt
    - tail file.txt
- **Searching**
    - find / -name file.txt
    - grep "word" file.txt
- **👤 User & Permissions**
    - whoami
    - chmod 755 file.sh
    - chown user file.txt
    - sudo command
- **Networking**
    - ifconfig
    - ip a
    - ping google.com
    - netstat -tulnp
## Dirsearch
### 🔹 Location in Kali
- /usr/share/dirsearch/
### 🔹 Basic Usage
- python3 dirsearch.py -u http://example.com
### 🔹 With Wordlist
- python3 dirsearch.py -u http://example.com -w wordlist.txt
### Extensions
- python3 dirsearch.py -u http://example.com -e php,html,txt
### Save Output
- python3 dirsearch.py -u http://example.com -o result.txt  