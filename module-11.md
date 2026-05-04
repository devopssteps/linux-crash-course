# 🎯 SSH & Remote Access

## 🧠 Concept 

**SSH (Secure Shell)** lets you:
 - ✔ Connect to remote servers securely
 - ✔ Run commands from your laptop
 - ✔ Manage cloud servers (AWS, Azure, etc.)

👉 In DevOps:

* You rarely work on local machine
* You always connect to remote servers

---

## 📡 What SSH Uses

* Port: **22**
* Protocol: Secure encrypted connection

---

# 💻 🧪 HANDS-ON DEMO

---

# 🔌 STEP 1: Connect to Remote Server

```bash id="ssh"
ssh ubuntu@your-server-ip
```

👉 Example:

```bash id="ssh2"
ssh ubuntu@54.123.45.67
```

---

> “This is how DevOps engineers log into servers in AWS, Azure, or any cloud.”

---

# 🔑 STEP 2: SSH with Key (IMPORTANT)

👉 Most common in cloud

```bash id="sshkey"
ssh -i mykey.pem ubuntu@your-server-ip
```

---

## 🔒 Fix key permission (VERY IMPORTANT)

```bash id="chmod"
chmod 400 mykey.pem
```

---

> “If your key permission is wrong, SSH will refuse connection — this is a very common issue.”

---

# 🔍 STEP 3: Check SSH Service

```bash id="sshstatus"
sudo systemctl status ssh
```

---

## 🔹 Start SSH (if not running)

```bash id="sshstart"
sudo systemctl start ssh
```

---

# 📂 STEP 4: Copy Files via SSH

## 🔹 Copy file to server

```bash id="scp1"
scp file.txt ubuntu@your-server-ip:/home/ubuntu/
```

---

## 🔹 Copy from server

```bash id="scp2"
scp ubuntu@your-server-ip:/home/ubuntu/file.txt .
```

---

# 🔁 STEP 5: SSH Without Password (Advanced)

## 🔹 Generate key

```bash id="keygen"
ssh-keygen
```

---

## 🔹 Copy key to server

```bash id="copykey"
ssh-copy-id ubuntu@your-server-ip
```

---

👉 Now login without password:

```bash id="login"
ssh ubuntu@your-server-ip
```

---

# ⚙️ STEP 6: SSH Config (Optional Advanced)

Edit:

```bash id="config"
nano ~/.ssh/config
```

👉 Example:

```text id="configtext"
Host myserver
  HostName 54.123.45.67
  User ubuntu
  IdentityFile mykey.pem
```

---

👉 Connect easily:

```bash id="short"
ssh myserver
```

---

# 🧠 DevOps Real-Life Scenarios

---

## 🔥 Scenario 1: Connect to AWS EC2

```bash id="real1"
ssh -i aws-key.pem ec2-user@public-ip
```

---

## 🔥 Scenario 2: Deploy code

```bash id="real2"
scp app.zip ubuntu@server:/var/www/
```

---

## 🔥 Scenario 3: Fix server issue remotely

```bash id="real3"
ssh ubuntu@server
```

---

# ⚠️ Common Issues (VERY IMPORTANT)

---

## ❌ Permission denied

✔ Fix:

```bash id="fix1"
chmod 400 mykey.pem
```

---

## ❌ Connection timeout

✔ Check:

* Security group
* Port 22 open

---

## ❌ Wrong user

✔ Use correct:

* ubuntu
* ec2-user

---

# 🔐 Security Best Practices

 - ✔ Use SSH key (not password)
 - ✔ Disable root login
 - ✔ Change default port (optional)

---

# 🧠 Quick Summary

| Command     | Purpose          |
| ----------- | ---------------- |
| ssh         | connect server   |
| scp         | transfer files   |
| ssh-keygen  | generate key     |
| ssh-copy-id | enable key login |
| systemctl   | manage SSH       |

---

> “SSH is the backbone of DevOps — if you can’t connect to servers, you can’t do anything.”

---

> “Master SSH, and you can control any server from anywhere in the world.”

---
> “Want to control a server from your laptop in seconds? This is how DevOps engineers do it.”

---

