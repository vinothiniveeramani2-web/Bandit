## 🛰️ Bandit Level 14 ➜ 15

### 🧷 Access Info
**Username:** bandit14  
**Password:** Obtained from previous level  
**Server:** bandit.labs.overthewire.org  
**Port:** 2220  

---

### 🎯 Challenge Overview
The password for the next level is not stored in a file.  
Instead, it is obtained by submitting the current level’s password to a service running on **localhost at port 30000**.  
The objective is to connect to the service, provide the correct password, and receive the next-level password.

---

### 🖼️ Terminal Snapshot
![Bandit Level 14 Screenshot](screenshots/level14.png)

---

### 🧭 How It Was Solved
A local network service is listening on port 30000.  
The `nc` (netcat) utility is used to connect to this service.  
Once connected, the current password is sent as input.  
If the password is correct, the service responds with the password for the next level.

---

### 💻 Commands Executed
- `nc localhost 30000`  

---

### 🔐 Password Retrieved
**8xCjmgokBGLhHFZLGE5Tmu4M2tKJQo**

---

### 📘 Explanation
- `nc` (netcat) is a networking tool used to read and write data over network connections.  
- Connecting to `localhost 30000` opens a session with the local service.  
- The current password is entered as input.  
- The service verifies the password and returns the password for Level 15 upon successful validation.

---

### 🧠 Key Takeaway
- Using `netcat` to interact with network services  
- Understanding localhost-based services  
- Sending input to listening ports  
- Retrieving data from network-based challenges  
