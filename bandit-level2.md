# OverTheWire: Bandit Level 2 → Level 3

## 🧠 Objective
Aquire the password for the next level. The file is has spaces in the name.

## 🔐 Credentials
- **Username**: `bandit2`
- **Password**: `263JGJPfgU6LtdEvgfWU1XP5yac29mFx`
- **Host**: `bandit.labs.overthewire.org`
- **Port**: `2220`

## 🛠️ Steps

1. **SSH into the server with previously aquired password**:
   ```bash
   ssh bandit2@bandit.labs.overthewire.org -p 2220
   → password: 
2. **Check files**:
   ```bash
   ls
   → spaces in this filename
   cat spaces\ in\ this\ filename
   → MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
**Level Complete** ✅

**NOTES:**
Because of the spaces we have to tell **cat** to search for the whole filename including the spaces. This is achieved with **'\\'**
