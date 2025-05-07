# OverTheWire: Bandit Level 6 → Level 7

## 🧠 Level Goal
The password for the next level is stored somewhere on the server and has all of the following properties:
- owned by user bandit7
- owned by group bandit6
- 33 bytes in size


## 🛠️ Steps

1. **I will leave out connecting via SSH from now on as it is identical in all levels**:

2. **Move to the root directory as we don't know where on the server the file is hiding**:
   ```bash
   cd /..
3. **Search for files matching the requirements and hide any errors**
   ```bash
   find -user bandit7 -group bandit6 -size 33c 2>/dev/null
   → ./var/lib/dpkg/info/bandit7.password
4. **Check the only file that returned to us**
   ```bash
   cat ./var/lib/dpkg/info/bandit7.password
   → morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
**Level Complete** ✅
