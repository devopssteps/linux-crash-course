# 🎯 1. Linux Directory Structure (/, /home, /etc, /var)

## 🧠 Concept 

Linux follows a **single root-based file system**.

👉 Everything starts from:

```bash id="rootdir"
/
```

This `/` is called the **root directory** — like the “C:\” in Windows.

---

## 📁 Important Directories (DevOps Perspective)

### 🔹 `/` (Root)

* Top-level directory
* All files & folders start here

---

### 🔹 `/home`

* User files & directories
* Example: `/home/ubuntu`

👉 Used for:

* Developer work
* Storing scripts, code

---

### 🔹 `/etc`

* Configuration files

👉 Used for:

* Nginx config
* SSH config
* System settings

---

### 🔹 `/var`

* Variable data (logs, runtime files)

👉 Used for:

* Logs → `/var/log`
* Web content → `/var/www`

---

# 💻 Hands-On Demo (SHOW THIS LIVE)

## 🔍 Step 1: Check current directory

```bash id="pwdcmd"
pwd
```

---

## 📂 Step 2: List root directories

```bash id="lscmd"
ls /
```

👉 Explain what you see:

* home
* etc
* var

---

## 📁 Step 3: Explore `/home`

```bash id="homecmd"
cd /home
ls
```

👉 Show:

* user folders

---

## ⚙️ Step 4: Explore `/etc`

```bash id="etccmd"
cd /etc
ls
```

👉 Show:

* nginx
* ssh

---

## 📊 Step 5: Explore `/var`

```bash id="varcmd"
cd /var
ls
```

👉 Then:

```bash id="varlogcmd"
cd /var/log
ls
```

👉 Show logs:

* syslog
* auth.log

---

> “As a DevOps engineer, you’ll mostly work inside `/etc` for configuration and `/var/log` for troubleshooting.”

---
# 🚀 2. Absolute vs Relative Path

## 🧠 Concept (Very Important)

### 🔹 Absolute Path

* Starts from `/` (root)
* Full path

👉 Example:

```bash id="abs"
cd /var/log
```

✔ Works from anywhere

---

### 🔹 Relative Path

* Based on current directory
* No `/` at start

👉 Example:

```bash id="rel"
cd var/log
```

❌ Works only if you are in correct location

---

## 💻 Hands-On Demo (VERY IMPORTANT)

### Step 1: Go to home

```bash id="home"
cd /home/ubuntu
pwd
```

---

### Step 2: Use Absolute Path

```bash id="absdemo"
cd /var/log
pwd
```

👉 Works from anywhere ✅

---

### Step 3: Go back

```bash id="back"
cd /home/ubuntu
```

---

### Step 4: Try Relative Path (will fail)

```bash id="reldemo"
cd var/log
```

👉 Explain:
❌ It fails because path doesn’t exist relative to current directory

---

### Step 5: Correct Relative Example

```bash id="reldemo2"
cd ..
```

👉 Moves one level up

```bash id="reldemo3"
cd ../..
```

👉 Moves two levels up

---

# 🔥 Visual Explanation (Say This)

👉 Absolute:

```text id="absvis"
/var/log
```

👉 Relative:

```text id="relvis"
../log
```

---

# 🎯 DevOps Real-Life Use Case

👉 Example:

```bash id="grep"
grep "error" /var/log/syslog
```

✔ Absolute path → always works

---

👉 Example script:

```bash id="script"
cd ../deploy
```

✔ Relative → used inside scripts

---




















