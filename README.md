# 🎯 🔥 Linux Crash Course for DevOps 

## ⏱️ Total Duration: 2 Hours

---

# 🚀 🧩 MODULE 1: Introduction + Setup 

### 📌 Topics:

* What is Linux (DevOps perspective)
* Why Linux is MUST for DevOps
* Distros (Ubuntu, Amazon Linux)

### 💻 Demo:

* Connect to server using SSH

```bash
ssh user@your-server-ip
```

---

# 📁 🧱 MODULE 2: File System Basics 

### 📌 Topics:

* Linux directory structure (`/`, `/home`, `/etc`, `/var`)
* Absolute vs relative path

### 💻 Commands:

```bash
pwd
ls
ls -la
cd
```

---

# 📂 📄 MODULE 3: File & Directory Management 

### 📌 Topics:

* Create, copy, move, delete files

### 💻 Commands:

```bash
touch file.txt
mkdir mydir
cp file.txt mydir/
mv file.txt newfile.txt
rm file.txt
rm -r mydir
```

---

# 🔐 🔑 MODULE 4: Permissions & Ownership 

### 📌 Topics:

* Read, write, execute
* chmod, chown

### 💻 Commands:

```bash
chmod 755 file.sh
chown ubuntu:ubuntu file.sh
```

👉 Explain:

* `rwx` meaning
* Numeric permissions (777, 755)

---

# 👥 👤 MODULE 5: Users & Groups 

### 📌 Topics:

* Add/remove users
* Groups

### 💻 Commands:

```bash
adduser devops
usermod -aG sudo devops
```

---

# 📦 📥 MODULE 6: Package Management 

### 📌 Topics:

* Install/update/remove packages

### 💻 Commands:

```bash
sudo apt update
sudo apt install nginx
sudo systemctl start nginx
```

---

# ⚙️ 🔄 MODULE 7: Process Management 

### 📌 Topics:

* Running processes
* Kill process

### 💻 Commands:

```bash
ps aux
top
kill -9 <pid>
```

---

# 🌐 🌍 MODULE 8: Networking Commands 

### 📌 Topics:

* IP, connectivity

### 💻 Commands:

```bash
ip a
ping google.com
curl ifconfig.me
netstat -tulnp
```

---

# 💾 📊 MODULE 9: Disk Management 

### 📌 Topics:

* Disk usage

### 💻 Commands:

```bash
df -h
du -sh *
```

---

# 📜 📂 MODULE 10: Logs & Monitoring 

### 📌 Topics:

* Log files (VERY IMPORTANT for DevOps)

### 💻 Commands:

```bash
tail -f /var/log/syslog
```

---

# 🔐 🔑 MODULE 11: SSH & Remote Access

### 📌 Topics:

* SSH basics
* Key-based authentication (concept)

---

# 🧠 🔥 MODULE 12: Shell Basics 

### 📌 Topics:

* Variables
* Simple scripting intro

### 💻 Demo:

```bash
#!/bin/bash
echo "Hello DevOps"
```

---

# ⚡ 🔥 MODULE 13: DevOps Real-Life Commands 

👉 This is your **USP (very important)**

### 💻 Show:

```bash
grep "error" app.log
find / -name "*.log"
chmod +x deploy.sh
```

👉 Explain:

* Debugging
* Automation

---

### 📌 Wrap-up:

* What to learn next:

  * Shell scripting
  * Docker
  * CI/CD

