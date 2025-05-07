# OverTheWire: Bandit Level 11 → Level 12
## 🧠 Level Goal
The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions
## 🛠️ Steps

1. **This required some research on wikipedia**:
   https://en.wikipedia.org/wiki/ROT13
2. **We could then shift all letters of the txt file and get the password**
   ```bash
   cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
   → The password is 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
**Level Complete** ✅
