## 🛰️ Bandit Stage 02 ➜ 03

### 🧷 Access Info
**Username:** bandit2  
**Server:** bandit.labs.overthewire.org  
**Port:** 2220  

---

### 🎯 Challenge Overview
The next password is stored in a file whose **filename contains spaces**, making it harder to read with a normal `cat` command.

---

### 🖼️ Terminal Snapshot
![Bandit Level 02 Screenshot](screenshots/level02.png)

---

### 🧭 How It Was Solved
Filenames with spaces must be **escaped** using backslashes (`\`).  
This prevents the shell from splitting the filename into multiple arguments.  
Using `--` ensures `cat` does not treat any part of the filename as an option.

---

### 💻 Commands Executed
```bash
ls
cat -- --spaces\ in\ this\ filename--
```

---

### 🔐 Password Retrieved
**MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx**

---

### 📘 Explanation
- The filename: `--spaces in this filename--` contains multiple spaces  
- Shell interprets each space as a separator  
- Adding `\` before each space keeps the filename as one string  
- Using `--` tells `cat` to stop processing options and treat everything after as a filename  
- The file contains the password for Level 03  

---

### 🧠 Key Takeaway
Learned how to handle files with **spaces and special characters** using:  
- Escape characters (`\`)  
- Safe filename handling  
- Proper command structuring to avoid shell misinterpretation  
