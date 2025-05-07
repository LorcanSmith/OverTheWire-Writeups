# OverTheWire: Bandit Level 1 → Level 2

## 🧠 Objective
Aquire the password for the next level. The file is name is -

## 🔐 Credentials
- **Username**: `bandit1`
- **Password**: `ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If`
- **Host**: `bandit.labs.overthewire.org`
- **Port**: `2220`

## 🛠️ Steps

1. **SSH into the server with previously aquired password**:
   ```bash
   ssh bandit1@bandit.labs.overthewire.org -p 2220
   → password: 
2. **Check files**:
   ```bash
   ls
   → -
   cat ./-
   → 263JGJPfgU6LtdEvgfWU1XP5yac29mFx
**Level Complete** ✅

**NOTES:**
Normally running:
```bash
cat -
```
tells **cat** to read from standard input (whatever we type next). So we need to tell cat to read **'-'** as a file name, hence the reason for the following:
```bash
cat ./-
