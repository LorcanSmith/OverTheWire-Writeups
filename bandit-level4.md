# OverTheWire: Bandit Level 4 → Level 5

## 🧠 Objective
Aquire the password for the next level. There are many files in the directory, find the one that is human-readable

## 🔐 Credentials
- **Username**: `bandit4`
- **Password**: `2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ`
- **Host**: `bandit.labs.overthewire.org`
- **Port**: `2220`

## 🛠️ Steps

1. **SSH into the server with previously aquired password**:
   ```bash
   ssh bandit4@bandit.labs.overthewire.org -p 2220
   → password: 
2. **Check files**:
   ```bash
   ls
   → inhere
   cd inhere
   ls
   → -file00  -file01  -file02  -file03  -file04  -file05  -file06  -file07  -file08  -file09
   find . | xargs file
   → .:         directory
    ./-file05: data
    ./-file03: data
    ./-file06: data
    ./-file02: data
    ./-file01: data
    ./-file09: data
    ./-file00: PGP Secret Sub-key -
    ./-file04: data
    ./-file08: data
    ./-file07: ASCII text
  3. **Check the file which contains ASCII text**
     ```bash
     cat ./-file07
     → 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
**Level Complete** ✅

**NOTES:**
As there were multiple files we used **find .** to search through all the files.
**xargs file** was then used to display the data type within each file found.
