# OverTheWire: Bandit Level 11 → Level 12
## 🧠 Level Goal
The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work. Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv (read the manpages!)## 🛠️ Steps

1. **First we moved the contents of the file to our local machine for easier access**:
   - `cat data.txt`
   - We simply copied the text and pasted it into a file on our local machine
     ![image](https://github.com/user-attachments/assets/191d63c2-b482-4c8c-ac38-ebde49874b51)

2. **Now it was time for lots of decompressing. This was actually a lot of fun**
   - First we reverted the hexdump
   - `~/Doc/Cyber/OverTheWire main !3 ?4 ❯ xxd -r data.txt data_reverse_hex.txt`
   - Then we checked what the file was, then decompress the file (renaming first if needed), and then repeating until we got a password.
   ```bash
    ~/Doc/Cyber/OverTheWire main !3 ?4 ❯ cat data_reverse_hex.txt
    <unreadable>
    ~/Doc/Cyber/OverTheWire main !3 ?4 ❯ file data_reverse_hex.txt 
    data_reverse_hex.txt: gzip compressed data, was "data2.bin", last modified: Thu Apr 10 14:22:57 2025, max compression, from Unix, original size modulo 2^32 585
    ~/Doc/Cyber/OverTheWire main !3 ?4 ❯ mv data_reverse_hex.txt data_reverse.gz
    ~/Doc/Cyber/OverTheWire main !3 ?4 ❯ file data_reverse.gz                   
    data_reverse.gz: gzip compressed data, was "data2.bin", last modified: Thu Apr 10 14:22:57 2025, max compression, from Unix, original size modulo 2^32 585
    ~/Doc/Cyber/OverTheWire main !3 ?4 ❯ gzip -d data_reverse.gz
    <unreadable>
    ~/Doc/Cyber/OverTheWire main !3 ?4 ❯ file data_reverse 
    data_reverse: bzip2 compressed data, block size = 900k
    ~/Doc/Cyber/OverTheWire main !3 ?4 ❯ bzip2 -d data_reverse 
    bzip2: Can't guess original name for data_reverse -- using data_reverse.out
    ~/Doc/Cyber/OverTheWire main !3 ?4 ❯ cat data_reverse
    ~/Doc/Cyber/OverTheWire main !3 ?4 ❯ cat data_reverse.out
    <unreadable>
    ~/Doc/Cyber/OverTheWire main !3 ?4 ❯ file data_reverse.out 
    data_reverse.out: gzip compressed data, was "data4.bin", last modified: Thu Apr 10 14:22:57 2025, max compression, from Unix, original size modulo 2^32 20480
    ~/Doc/Cyber/OverTheWire main !3 ?4 ❯ mv data_reverse.out data.gz
    ~/Doc/Cyber/OverTheWire main !3 ?4 ❯ gzip -d data.gz
    ~/Doc/Cyber/OverTheWire main !3 ?4 ❯ cat data
    <unreadable>
    ~/Doc/Cyber/OverTheWire main !3 ?4 ❯ file data
    data: POSIX tar archive (GNU)
    ~/Doc/Cyber/OverTheWire main !3 ?4 ❯ tar -xf data 
    ~/Doc/Cyber/OverTheWire main !3 ?4 ❯ cat data5.bin
    <unreadable>
    ~/Doc/Cyber/OverTheWire main !3 ?4 ❯ file data5.bin 
    data5.bin: POSIX tar archive (GNU)
    ~/Doc/Cyber/OverTheWire main !3 ?4 ❯ tar -xf data5.bin
    ~/Doc/Cyber/OverTheWire main !3 ?4 ❯ cat data6.bin
    <unreadable>
    ~/Doc/Cyber/OverTheWire main !3 ?4 ❯ file data6.bin 
    data6.bin: bzip2 compressed data, block size = 900k
    ~/Doc/Cyber/OverTheWire main !3 ?4 ❯ bzip2 -d data6.bin 
    bzip2: Can't guess original name for data6.bin -- using data6.bin.out
    ~/Doc/Cyber/OverTheWire main !3 ?4 ❯ cat data6.bin.out
    <unreadable>
    ~/Doc/Cyber/OverTheWire main !3 ?4 ❯ file data6.bin.out 
    data6.bin.out: POSIX tar archive (GNU)
    ~/Doc/Cyber/OverTheWire main !3 ?4 ❯ tar -xf data6.bin.out
    ~/Doc/Cyber/OverTheWire main !3 ?4 ❯ cat data8.bin
    <unreadable>
    /Doc/Cyber/OverTheWire main !3 ?4 ❯ file data8.bin 
    data8.bin: gzip compressed data, was "data9.bin", last modified: Thu Apr 10 14:22:57 2025, max compression, from Unix, original size modulo 2^32 49
    ~/Doc/Cyber/OverTheWire main !3 ?4 ❯ mv data8.bin data8.gz
    ~/Doc/Cyber/OverTheWire main !3 ?4 ❯ gzip -d data8.gz
    ~/Doc/Cyber/OverTheWire main !3 ?4 ❯ cat data8
    The password is FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn

**Level Complete** ✅
