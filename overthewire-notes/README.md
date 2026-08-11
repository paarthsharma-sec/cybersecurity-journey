# OverTheWire: Bandit Writeups

## Bandit Level 0
### Objective
Connect to server via SSH
### Commands Used
ssh bandit0@bandit.labs.overthewire.org -p 2220
### What I Learned
- SSH used to remotely connect to servers
- Syntax: ssh username@hostname -p portnumber
- Default SSH port is 22, this server uses 2220

## Bandit Level 1
### Objective
Read a file named - (dash)
### Commands Used
cat ./-
### What I Learned
- Files starting with - cant be opened with just cat filename
- Use ./ before filename to read special character files

## Bandit Level 2
### Objective
Read a file with spaces in filename
### Commands Used
cat "spaces in this filename"
### What I Learned
- Files with spaces need quotes around the name
- Can also use backslash before each space

## Bandit Level 3
### Objective
Find hidden file inside a directory
### Commands Used
cd inhere
ls -la
cat .hidden
### What I Learned
- ls -la shows hidden files starting with dot
- Hidden files start with . in Linux

## Bandit Level 4
### Objective
Find only human readable file in directory
### Commands Used
file ./-file0*
cat ./-file07
### What I Learned
- file command shows what type each file is
- Human readable files show as ASCII text

## Bandit Level 5
### Objective
Find file with specific properties
### Commands Used
find . -type f -size 1033c ! -executable
### What I Learned
- find command searches files by properties

## Bandit Level 6
### Objective
Find file owned by specific user and group
### Commands Used
find / -user bandit7 -group bandit6 -size 33c
### What I Learned
- find command searches entire system with /
- -user and -group flags filter by ownership
- Redirect errors using 2>/dev/null to clean output

## Bandit Level 7
### Objective
Find password next to word "millionth" in file
### Commands Used
grep "millionth" data.txt
### What I Learned
- grep searches for specific text inside files
- Syntax: grep "keyword" filename

## Bandit Level 8
### Objective
Find line that appears only once in file
### Commands Used
sort data.txt | uniq -u
### What I Learned
- sort organizes lines alphabetically
- uniq -u shows only unique lines
- Pipe | chains commands together

## Bandit Level 9
### Objective
Find human readable strings in file
### Commands Used
strings data.txt | grep "=="
### What I Learned
- strings extracts readable text from binary files
- Combining strings with grep finds specific patterns

## Bandit Level 10
### Objective
Decode Base64 encoded file
### Commands Used
base64 -d data.txt
### What I Learned
- Base64 is an encoding scheme not encryption
- base64 -d decodes Base64 encoded text
- Common encoding used in cybersecurity
- -size searches by file size
- ! -executable means not executable
- -type f means regular file only
