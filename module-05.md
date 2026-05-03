# 🎯 Linux Users & Groups

## 🧠 Concept 

Linux is a **multi-user system**.

👉 That means:

* Multiple users can use the same server
* Each user has **permissions & access control**

---

## 👤 What is a User?

A **user** is an account that can:

* Login to the system
* Run commands
* Own files

👉 Example:

* `ubuntu`
* `root`

---

## 👥 What is a Group?

A **group** is a collection of users.

👉 Used to:

* Manage permissions easily
* Give access to multiple users at once

---

# 💻 🧪 HANDS-ON DEMO

## 🔍 Step 1: Check Current User

```bash id="whoami"
whoami
```

---

## 🔍 Step 2: Check User ID & Groups

```bash id="idcmd"
id
```

👉 Example output:

```text id="idout"
uid=1000(ubuntu) gid=1000(ubuntu) groups=1000(ubuntu),27(sudo)
```

👉 Explain:

* `uid` → user ID
* `gid` → group ID
* `groups` → user belongs to multiple groups

---

# 👤 Step 3: Create a New User

```bash id="adduser"
sudo adduser devops
```

👉 It will ask:

* Password
* User details

---

## 🔍 Verify

```bash id="lsusers"
ls /home
```

👉 You’ll see:

```text id="homeout"
ubuntu devops
```

---

# 🔄 Step 4: Switch User

```bash id="switchuser"
su - devops
```

👉 Check:

```bash id="whoami2"
whoami
```

---

# 👥 Step 5: Create a Group

```bash id="addgroup"
sudo groupadd devteam
```

---

# ➕ Step 6: Add User to Group

```bash id="usermod"
sudo usermod -aG devteam devops
```

👉 Verify:

```bash id="groups"
groups devops
```

---

# 🔐 Step 7: Give Sudo Access 

```bash id="sudo"
sudo usermod -aG sudo devops
```

👉 Explain:

* Now user can run admin commands

---

# ❌ Step 8: Delete User 

```bash id="deluser"
sudo deluser devops
```

---

# 🧠 DevOps Real-Life Use Cases

## 🔹 Case 1: Multiple Devs working on same server

👉 Create group:

```bash id="real1"
sudo groupadd developers
```

👉 Add users:

```bash id="real2"
sudo usermod -aG developers user1
sudo usermod -aG developers user2
```

---

## 🔹 Case 2: Web server permissions

```bash id="real3"
sudo chown -R www-data:www-data /var/www/html
```

👉 `www-data` = web server user

---

## 🔹 Case 3: Fix permission issue

```bash id="real4"
sudo chown -R ubuntu:ubuntu project/
```

---

# ⚠️ Important Concepts

## 🔴 root user

* Super admin
* Full access

```bash id="root"
sudo su
```

---

## 🟡 sudo

* Run command as admin

```bash id="sudocmd"
sudo apt update
```

---

# 🧠 Quick Summary

| Command  | Purpose      |
| -------- | ------------ |
| adduser  | create user  |
| groupadd | create group |
| usermod  | modify user  |
| groups   | check groups |
| su       | switch user  |

---

> In DevOps, managing users and groups is critical because multiple engineers and services share the same server.

---

> If you understand users, groups, and permissions together, you can fully control any Linux system.

---

> If you don’t understand Linux users and groups, you can break your server in seconds.

---

