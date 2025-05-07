# OverTheWire: Bandit Level 5 → Level 6

## 🧠 Objective
Aquire the password for the next level. Password is stored in a file which has all of the following properties:
- Human-readable
- 1033 bytes in size
- not executable


## 🔐 Credentials
- **Username**: `bandit5`
- **Password**: `4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw`
- **Host**: `bandit.labs.overthewire.org`
- **Port**: `2220`

## 🛠️ Steps

1. **SSH into the server with previously aquired password**:
   ```bash
   ssh bandit5@bandit.labs.overthewire.org -p 2220
   → password: 
2. **Search files**:
   ```bash
   ls
   → inhere
   cd inhere
   ls
   → maybehere00  maybehere03  maybehere06  maybehere09  maybehere12  maybehere15  maybehere18
    maybehere01  maybehere04  maybehere07  maybehere10  maybehere13  maybehere16  maybehere19
    maybehere02  maybehere05  maybehere08  maybehere11  maybehere14  maybehere17
   find . -size 1033c
   → ./maybehere07/.file2
  3. **Check the only file which matches the size**
     ```bash
     cat ./maybehere07/.file2
     → HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
**Level Complete** ✅

**NOTES:**
Was lucky there was only one file matching the size requirements. The use of **c** in **-size 1033c** tells it to search in bytes.
