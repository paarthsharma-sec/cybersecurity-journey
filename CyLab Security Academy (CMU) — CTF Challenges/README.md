# CyLab Security Academy — CTF Writeups
### Platform: Carnegie Mellon University (CMU)

## Progress Tracker
| Category | Status | Completed |
|----------|--------|-----------|
| General Skills | ✅ Completed | 20/20 |
| Cryptography | ✅ Completed | 20/20 |
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


### Challenge 6 — Tab Tab Attack
**What I did:** Used tab completion to navigate 
deeply nested directories and find the flag
**What I Learned:**
- Tab key auto-completes file/directory names
- Deeply nested directories are common in CTF
- cd and tab together navigate quickly


### Challenge 7 — Magikarp Ground Mission
**What I did:** SSH'd into server and navigated 
between directories to collect flag parts
**What I Learned:**
- Flags can be split across multiple locations
- SSH into remote machines for challenges
- cat and cd used together to find distributed flags


### Challenge 8 — First Grep
**What I did:** Used grep to search through large 
file and find the flag
**What I Learned:**
- grep searches text patterns inside files
- Essential command for finding specific strings
- grep "picoCTF" filename finds flags instantly


### Challenge 9 — Bases
**What I did:** Decoded Base64 encoded string 
to reveal the flag
**What I Learned:**
- Base64 is common encoding in cybersecurity
- echo "string" | base64 -d decodes Base64
- Encoding is not encryption — easily reversible


### Challenge 10 — Plumbing
**What I did:** Connected to server using netcat 
and piped output to grep to find flag
**What I Learned:**
- Pipe operator | chains command outputs
- grep filters specific output from commands
- nc combined with grep is powerful for CTF


### Challenge 11 — Blame Game
**What I did:** Searched git history to find 
who introduced the bug and find the flag
**What I Learned:**
- git log shows commit history
- git blame tracks who changed each line
- Version control reveals hidden information


### Challenge 12 — Convertme
**What I did:** Converted number between 
different bases to find the flag
**What I Learned:**
- Numbers exist in binary, octal, decimal, hex
- Python bin(), oct(), hex() convert between bases
- Base conversion is fundamental in cybersecurity


### Challenge 13 — Fixme1
**What I did:** Fixed syntax error in Python 
script to make it print the flag
**What I Learned:**
- Reading error messages finds the problem
- Indentation errors are common in Python
- Debugging code is a core security skill


### Challenge 14 — Fixme2
**What I did:** Fixed logical error in Python 
script to reveal the flag
**What I Learned:**
- Logical errors don't crash code but give wrong output
- Reading code carefully finds logical mistakes
- Understanding code flow is essential


### Challenge 15 — Glitch Cat
**What I did:** Connected to server and 
decoded obfuscated Python output to get flag
**What I Learned:**
- Code can be obfuscated to hide its purpose
- chr() converts ASCII numbers to characters
- eval() executes string as Python code


### Challenge 16 — HashingJobApp
**What I did:** Identified hash types and 
submitted correct hashes to get flag
**What I Learned:**
- MD5, SHA1, SHA256 are common hash types
- Python hashlib generates hashes
- Hashing is fundamental in cybersecurity


### Challenge 17 — Codebook
**What I did:** Used provided codebook file 
to decode secret message and find flag
**What I Learned:**
- Substitution ciphers replace letters with symbols
- Codebooks map one character to another
- Simple ciphers are foundation of cryptography


### Challenge 18 — Binary Search
**What I did:** Used binary search logic to 
guess correct number efficiently and get flag
**What I Learned:**
- Binary search eliminates half possibilities each step
- Much faster than linear search
- Core algorithm used in real security tools


### Challenge 19 — Undo
**What I did:** Completed 5 decoding tasks 
in sequence to reveal the flag
**Tasks completed:**
- Base64 decoding
- String reversal
- ROT13 cipher decoding
- A to Z translation
- Additional encoding tasks
**What I Learned:**
- Multiple encoding layers can be stacked together
- Each encoding type has specific decode method
- base64 -d, rev, tr commands handle these tasks
- Real CTF challenges chain multiple techniques


### Challenge 20 — My Git
**What I did:** Used git commands to recover 
deleted file from commit history containing flag
**Commands Used:**
- git log --all
- git checkout
- git show
**What I Learned:**
- Git never truly deletes committed files
- git log --all shows complete commit history
- Deleted files recoverable through git history
- Critical forensics skill for real investigations


- ## Cryptography
- 
### Challenge 1 — Mod 26
**What I did:** Applied ROT13 cipher to decode the flag
**What I Learned:**
- ROT13 shifts letters by 13 positions
- tr command handles ROT13 in terminal
- Caesar cipher family is common in CTF

---

### Challenge 2 — Easy1
**What I did:** Used Vigenere cipher table to decode message
**What I Learned:**
- Vigenere cipher uses a keyword for encoding
- Table lookup decodes each character
- Polyalphabetic ciphers are harder than Caesar

---

### Challenge 3 — Caesar
**What I did:** Brute forced Caesar cipher shifts to find flag
**What I Learned:**
- Caesar cipher shifts alphabet by fixed number
- Only 25 possible shifts — easy to brute force
- frequency analysis helps identify shift

---

### Challenge 4 — 13
**What I did:** Decoded ROT13 encoded flag
**What I Learned:**
- ROT13 is self-inverse — encode and decode same operation
- echo "text" | tr 'A-Za-z' 'N-ZA-Mn-za-m'
- Very common encoding in CTF challenges

---

### Challenge 5 — The Numbers
**What I did:** Converted numbers to letters using A=1 Z=26
**What I Learned:**
- Simple substitution cipher using number positions
- A=1, B=2... Z=26 is classic beginner crypto
- Pattern recognition key in cryptography


### Challenge 6 — Substitution0
**What I did:** Decoded substitution cipher 
by analyzing letter frequency patterns
**What I Learned:**
- Substitution ciphers replace each letter consistently
- Frequency analysis breaks substitution ciphers
- E, T, A are most common letters in English

---

### Challenge 7 — Substitution1
**What I did:** Partially decoded substitution 
cipher using known plaintext patterns
**What I Learned:**
- Known plaintext attacks use partial information
- Word patterns help identify substitutions
- Common words like "the" reveal multiple letters

---

### Challenge 8 — Substitution2
**What I did:** Completed full substitution 
cipher decode using combined techniques
**What I Learned:**
- Combining frequency analysis and pattern matching
- Full alphabet mapping breaks any substitution cipher
- Systematic approach beats random guessing

---

### Challenge 9 — Credstuff
**What I did:** Used wordlist to crack 
hashed credentials from leaked database
**What I Learned:**
- Real databases store hashed passwords
- Wordlist attacks match common passwords to hashes
- MD5 hashes are easily crackable with wordlists
- Credential stuffing is real world attack vector

---

### Challenge 10 — Morse Code
**What I did:** Decoded audio file 
containing morse code to find flag
**What I Learned:**
- Morse code represents letters as dots and dashes
- Audio files can contain encoded messages
- Online morse decoders handle audio conversion

---

### Challenge 11 — Dachshund Attacks
**What I did:** Exploited weak RSA key using 
Wiener attack to recover private key
**What I Learned:**
- RSA security depends on large prime numbers
- Wiener attack breaks RSA with small private exponents
- Weak RSA keys are vulnerable to mathematical attacks

---

### Challenge 12 — Mini RSA
**What I did:** Exploited small RSA exponent 
to decrypt ciphertext without private key
**What I Learned:**
- Small public exponents make RSA vulnerable
- Cube root attack works when exponent is 3
- Proper RSA requires large random exponents

---

### Challenge 13 — Basic Mod1
**What I did:** Decoded message using 
modulo 37 operation to get plaintext
**What I Learned:**
- Modular arithmetic is foundation of cryptography
- mod operation finds remainder after division
- Character mapping with modulo creates simple ciphers

---

### Challenge 14 — Basic Mod2
**What I did:** Decoded message using 
modular inverse operation
**What I Learned:**
- Modular inverse reverses modular multiplication
- Extended Euclidean algorithm finds modular inverse
- More complex than Mod1 but same concept

---

### Challenge 15 — Pixelated
**What I did:** Combined two image shares 
using XOR to reveal hidden flag
**What I Learned:**
- Visual cryptography splits secret into shares
- XOR operation combines shares to reveal secret
- Images can hide information visually

---

### Challenge 16 — New Caesar
**What I did:** Decoded custom Caesar variant 
using base16 encoding and shifted alphabet
**What I Learned:**
- Caesar variants use different alphabets or bases
- base16 encoding uses only letters a-p
- Custom ciphers combine multiple techniques

---

### Challenge 17 — Vigenere
**What I did:** Decoded Vigenere cipher 
by finding the key through Kasiski examination
**What I Learned:**
- Vigenere uses repeating keyword for encoding
- Kasiski examination finds key length
- Index of coincidence confirms key length

---

### Challenge 18 — Railfence
**What I did:** Decoded railfence cipher 
by reconstructing the zigzag pattern
**What I Learned:**
- Railfence writes message in zigzag across rails
- Number of rails is the key
- Transposition ciphers rearrange rather than replace

---

### Challenge 19 — b00tl3gRSA2
**What I did:** Exploited weak RSA with 
small prime difference to factor the modulus
**What I Learned:**
- RSA primes must be far apart in value
- Fermat factorization works when primes are close
- Strong RSA requires carefully chosen large primes

---

### Challenge 20 — b00tl3gRSA3
**What I did:** Exploited RSA with common 
factor between two different moduli
**What I Learned:**
- Sharing prime factors between RSA keys is catastrophic
- GCD attack finds common factors instantly
- Each RSA key must use completely unique primes

