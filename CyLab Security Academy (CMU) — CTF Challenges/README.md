# CyLab Security Academy — CTF Writeups
### Platform: Carnegie Mellon University (CMU)

## Progress Tracker
| Category | Status | Completed |
|----------|--------|-----------|
| General Skills | 🔄 In Progress | 3/? |
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

