# 🎯 Linux Package Management

## 🧠 Concept 

**Package management** is how you:

* Install software
* Update software
* Remove software

👉 In DevOps, this is used **daily** to:
 - ✔ Install Nginx, Docker, Git
 - ✔ Update systems
 - ✔ Manage dependencies

---

# 🧩 What is a Package?

A **package** = pre-built software bundle

👉 Example:

* nginx
* docker
* git

---

# ⚙️ Different Package Managers

## 🟢 Ubuntu / Debian

👉 Uses:

```bash
apt
```

---

## 🟡 Amazon Linux / RHEL

👉 Uses:

```bash
yum   (older)
dnf   (newer)
```

---

# 💻 🧪 HANDS-ON DEMO (Ubuntu / Amazon Linux)

---

# 🚀 STEP 1: Update Package List (VERY IMPORTANT)

```bash id="update"
sudo apt update
```

👉 Explain:

* Refreshes package list
* Must run before installing

---

# 📦 STEP 2: Install Package

```bash id="install"
sudo apt install nginx -y
```

👉 `-y` = auto yes

---

# 🔍 Verify Installation

```bash id="verify"
nginx -v
```

---

# ▶️ STEP 3: Start Service

```bash id="start"
sudo systemctl start nginx
```

---

# 📊 Check Status

```bash id="status"
sudo systemctl status nginx
```

---

# 🌐 Test in Browser

```bash id="curl"
curl localhost
```

---

# 🔄 STEP 4: Update Packages

```bash id="upgrade"
sudo apt upgrade -y
```

👉 Updates all installed software

---

# ❌ STEP 5: Remove Package

```bash id="remove"
sudo apt remove nginx
```

---

# 🧹 Remove completely (config + files)

```bash id="purge"
sudo apt purge nginx
```

---

# 🔍 STEP 6: Search Package

```bash id="search"
apt search nginx
```

---

# 📋 STEP 7: List Installed Packages

```bash id="list"
apt list --installed
```

---

# 🟡 Amazon Linux / RHEL (IMPORTANT DIFFERENCE)

👉 Install:

```bash id="yuminstall"
sudo yum install nginx -y
```

👉 Update:

```bash id="yumupdate"
sudo yum update -y
```

---

# 🧠 DevOps Real-Life Examples 

## 🔹 Install Docker

```bash id="real1"
sudo apt install docker.io -y
```

---

## 🔹 Install Git

```bash id="real2"
sudo apt install git -y
```

---

## 🔹 Fix broken package

```bash id="real3"
sudo apt --fix-broken install
```

---

## 🔹 Install specific version

```bash id="real4"
sudo apt install nginx=1.18.*
```

---

# ⚠️ Important Tips

 - ✔ Always run `update` before install
 - ✔ Use `-y` for automation
 - ✔ Remove unused packages:

```bash id="cleanup"
sudo apt autoremove
```

---

# 🧠 DevOps Use Case 

👉 Example:

* Deploy app → need nginx
* CI/CD pipeline → install dependencies

---

> Package management is the first thing DevOps engineers use when setting up any server.

---

> If you know package management, you can install and manage any software on any Linux server.

---

> If you don’t know how to install software on Linux, you can’t do DevOps.

---

# 🏆 Quick Summary

| Task    | Command       |
| ------- | ------------- |
| Update  | `apt update`  |
| Install | `apt install` |
| Remove  | `apt remove`  |
| Upgrade | `apt upgrade` |

---
