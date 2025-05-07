# OverTheWire: Bandit Level 9 → Level 10
## 🧠 Level Goal
The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

## 🛠️ Steps

1. **First we tried**:
   ```bash
   grep ==* data.txt
   → grep: data.txt: binary file matches
This was unsuccessful so we had to try a different approach
2. **Search for valid strings first**
```bash
    strings data.txt | grep ==*
      → ,k=?
        @k*=
        ========== the
        #e=in
        g+=ypF
        ea=+
        K>=*<
        ========== password{k
        =========== is
        1R=j/
        e=<2g%
        +G/YD=
        =wDk
        =3?lOt
        ========== FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
        =D!f
        H =sS
```
**Level Complete** ✅
