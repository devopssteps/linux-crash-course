# 🎯 Linux Permissions & Ownership

## 🧠 Concept 

In Linux, **every file and directory has:**

1. **Owner (user)**
2. **Group**
3. **Permissions**

👉 These control:
 - ✔ Who can read
 - ✔ Who can write
 - ✔ Who can execute

---

# 🧩 Permission Types

| Symbol | Meaning |
| ------ | ------- |
| r      | read    |
| w      | write   |
| x      | execute |

---

# 👥 Permission Levels

| Who | Meaning      |
| --- | ------------ |
| u   | user (owner) |
| g   | group        |
| o   | others       |

---

# 💻 🧪 HANDS-ON DEMO

## 🔍 Step 1: Check Permissions

```bash id="lsperm"
ls -l
```

👉 Example output:

```text id="lsout"
-rw-r--r-- 1 ubuntu ubuntu 0 file1.txt
```

---

## 🧠 Explanation

```text id="break"
-rw-r--r--
```

Breakdown:

* First `-` → file type
* Next 3 → **owner (rw-)**
* Next 3 → **group (r--)**
* Next 3 → **others (r--)**

---

> “This means owner can read/write, but others can only read.”

---

# 🔐 Step 2: Change Permissions (chmod)

## 🔹 Add execute permission

```bash id="chmod1"
chmod +x file1.txt
```

---

## 🔹 Remove write permission

```bash id="chmod2"
chmod -w file1.txt
```

---

## 🔹 Numeric Mode 

```bash id="chmod3"
chmod 755 file1.txt
```

👉 Explain:

* 7 = rwx (4+2+1)
* 5 = r-x (4+0+1)

---

### 🔢 Permission Table

| Number | Permission |
| ------ | ---------- |
| 7      | rwx        |
| 6      | rw-        |
| 5      | r-x        |
| 4      | r--        |

---

> “In DevOps, 755 is very common for scripts and applications.”

---

# 👤 Step 3: Change Ownership (chown)

## 🔹 Change owner

```bash id="chown1"
sudo chown devops file1.txt
```

---

## 🔹 Change owner + group

```bash id="chown2"
sudo chown devops:devops file1.txt
```

---

👉 Verify:

```bash id="verifyown"
ls -l
```

---

# 👥 Step 4: Change Group (chgrp)

```bash id="chgrp"
chgrp devops file1.txt
```

---

# 🚀 DevOps Real-Life Examples 

## 🔹 Make script executable

```bash id="real1"
chmod +x deploy.sh
```

---

## 🔹 Secure SSH key

```bash id="real2"
chmod 600 ~/.ssh/id_rsa
```

👉 Explanation:

* Only owner can read/write
* Others cannot access

---

## 🔹 Fix permission issue (common)

```bash id="real3"
sudo chown -R ubuntu:ubuntu /var/www/html
```

---

# ⚠️ Important Warnings

## ❌ Never do this blindly:

```bash id="danger"
chmod 777 file.txt
```

👉 Why dangerous?

* Everyone gets full access
* Security risk

---

# 🧠 Quick Summary

| Command | Use               |
| ------- | ----------------- |
| chmod   | change permission |
| chown   | change owner      |
| chgrp   | change group      |

---

# 🎯 DevOps Use Case

👉 Example:

* App not working → permission issue
* Fix:

```bash id="fix"
chmod -R 755 /app
```

---

> “Permissions are one of the most common issues in DevOps — if you master this, you can solve real production problems.”

---

> “90% of DevOps errors come from permission issues — let me show you how to fix them.”

---
