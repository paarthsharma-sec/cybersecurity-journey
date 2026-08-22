# CyLab Security Academy — CTF Writeups
### Platform: Carnegie Mellon University (CMU)

## Progress Tracker
| Category | Status | Completed |
|----------|--------|-----------|
| General Skills | 🔄 In Progress | 5/? |
| Cryptography | 📌 Upcoming | 0 |
| Web Exploitation | 📌 Upcoming | 0 |
| Forensics | 📌 Upcoming | 0 |

---

## General Skills

### Challenge 1 — Obedient Cat
**What I did:** Downloaded the file and opened it to find the flag directly inside
**What I Learned:**
- CTF flags are hidden inside files, systems or code
- Always check file contents first before anything complex
- Flag format is always picoCTF{...}


### Challenge 2 — Wave a Flag
**What I did:** Downloaded the binary file, ran it with -h flag
**Command Used:** ./warm -h
**What I Learned:**
- Binary files need execute permission to run
- -h or --help shows available options for any program
- Always try -h on unknown binaries in CTF challenges


### Challenge 3 — Python Wrangling
**What I did:** Used Python script with correct arguments to decrypt flag
**What I Learned:**
- Python scripts take arguments from command line
- sys.argv handles command line arguments in Python
- Always read the script before running it


### Challenge 4 — Nice netcat
**What I did:** Connected to server using netcat, 
received ASCII numbers, used Python to convert 
them to readable characters
**Command Used:** nc mercury.picoctf.net 7449
**What I Learned:**
- netcat (nc) connects to remote servers and ports
- Servers can send data in ASCII number format
- chr() in Python converts numbers to characters
- ASCII encoding is commonly used in CTF challenges

### Challenge 5 — Static ain't always noise
**What I did:** Analyzed a binary file and script 
to extract the flag
**What I Learned:**
- Static files can contain readable strings
- strings command extracts readable text from binaries
- grep helps filter specific patterns from output
- Not all noise is useless — hidden data exists in files
