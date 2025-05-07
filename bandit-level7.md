# OverTheWire: Bandit Level 7 → Level 8

## 🧠 Level Goal
The password for the next level is stored in the file data.txt next to the word millionth

## 🛠️ Steps

1. **Search the data.txt file for the password**:
   ```bash
   ls
   → data.txt
   grep millionth* data.txt
   → millionth	dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
   
**Level Complete** ✅

**Notes:**
We use **grep** to search for the word **millionth** and use the asterix to indicate we want to include any data that contains that word.
