# OverTheWire: Bandit Level 8 → Level 9

## 🧠 Level Goal
The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

## 🛠️ Steps

1. **Sort the contents of data.txt and then search for unique lines**:
   ```bash
   ls
   → data.txt
   sort data.txt | uniq -u
   → 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
**Level Complete** ✅

**Notes:**
We use **sort** to arrange the file alphabetically. We then use **uniq -u** to find unique strings.
