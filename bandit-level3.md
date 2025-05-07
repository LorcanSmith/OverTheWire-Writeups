# OverTheWire: Bandit Level 3 → Level 4

## 🧠 Objective
Aquire the password for the next level. The file is hidden.

## 🔐 Credentials
- **Username**: `bandit3`
- **Password**: `MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx`
- **Host**: `bandit.labs.overthewire.org`
- **Port**: `2220`

## 🛠️ Steps

1. **SSH into the server with previously aquired password**:
   ```bash
   ssh bandit3@bandit.labs.overthewire.org -p 2220
   → password: 
2. **Check files**:
   ```bash
   ls
   → inhere
   cd inhere
   ls -a
   → ...Hiding-From-You
   cat ...Hiding-From-You
   → 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
**Level Complete** ✅

**NOTES:**
To view view hidden files we tell **'ls'** to list all files:
```bash
ls -a
