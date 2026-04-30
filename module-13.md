# 🎯 DevOps Real-Life Linux Commands

## 🧠 Concept (Why This Matters)

In real DevOps work, you don’t just run commands randomly — you:
 - ✔ Debug issues
 - ✔ Deploy applications
 - ✔ Monitor servers
 - ✔ Fix production problems

👉 These are **battle-tested commands used daily in real jobs**

---

# 💻 🧪 HANDS-ON REAL SCENARIOS

---

# 🔥 SCENARIO 1: Server is Down (First Response)

## Step 1: Check server health

```bash id="health1"
uptime
```

👉 Shows load average

---

## Step 2: Check CPU usage

```bash id="health2"
top
```

---

## Step 3: Check memory

```bash id="health3"
free -m
```

---

## Step 4: Check disk

```bash id="health4"
df -h
```

---

> “Whenever a server is down, these 4 commands are your first checks.”

---

# 🔥 SCENARIO 2: Application Not Working

## Step 1: Check process

```bash id="app1"
ps aux | grep nginx
```

---

## Step 2: Check port

```bash id="app2"
ss -tulnp | grep 80
```

---

## Step 3: Restart service

```bash id="app3"
sudo systemctl restart nginx
```

---

## Step 4: Check logs

```bash id="app4"
tail -f /var/log/nginx/error.log
```

---

> “Most production issues are solved by checking process, port, and logs.”

---

# 🔥 SCENARIO 3: High Disk Usage

## Step 1: Check disk

```bash id="disk1"
df -h
```

---

## Step 2: Find large files

```bash id="disk2"
du -sh /var/*
```

---

## Step 3: Clean logs

```bash id="disk3"
sudo rm -rf /var/log/*.gz
```

---

# 🔥 SCENARIO 4: Network Issue

## Step 1: Check connectivity

```bash id="net1"
ping google.com
```

---

## Step 2: Check DNS

```bash id="net2"
nslookup google.com
```

---

## Step 3: Check open ports

```bash id="net3"
ss -tulnp
```

---

## Step 4: Test API

```bash id="net4"
curl http://localhost
```

---

# 🔥 SCENARIO 5: Deploy Application

## Step 1: Clone code

```bash id="deploy1"
git clone https://github.com/user/app.git
```

---

## Step 2: Go to project

```bash id="deploy2"
cd app
```

---

## Step 3: Build Docker image

```bash id="deploy3"
docker build -t myapp .
```

---

## Step 4: Run container

```bash id="deploy4"
docker run -d -p 80:80 myapp
```

---

# 🔥 SCENARIO 6: Fix Permission Issue

## Step 1: Check permissions

```bash id="perm1"
ls -l
```

---

## Step 2: Fix ownership

```bash id="perm2"
sudo chown -R ubuntu:ubuntu /var/www/html
```

---

## Step 3: Fix permissions

```bash id="perm3"
chmod -R 755 /var/www/html
```

---

# 🔥 SCENARIO 7: Log Debugging

## Step 1: Live logs

```bash id="log1"
tail -f /var/log/syslog
```

---

## Step 2: Filter error

```bash id="log2"
grep "error" /var/log/syslog
```

---

# 🔥 SCENARIO 8: SSH & Remote Fix

## Connect to server

```bash id="ssh1"
ssh -i key.pem ubuntu@server-ip
```

---

## Copy file

```bash id="scp1"
scp file.txt ubuntu@server:/home/ubuntu/
```

---

# ⚡ MOST IMPORTANT COMMANDS (MUST KNOW)

| Area    | Commands          |
| ------- | ----------------- |
| System  | uptime, top, free |
| Disk    | df, du            |
| Process | ps, kill          |
| Network | ping, curl, ss    |
| Logs    | tail, grep        |
| Service | systemctl         |
| File    | cp, mv, rm        |

---

# 🎯 Real DevOps Workflow (IMPORTANT)

👉 When issue happens:

1. Check system (CPU, memory, disk)
2. Check service (running or not)
3. Check logs
4. Fix and restart

---

> “DevOps is not about knowing commands — it’s about knowing which command to run when something breaks.”

---

> “If you master these real-life commands, you can troubleshoot any production issue like a pro.”

---

> “Your server is down at 2 AM — these are the exact commands DevOps engineers use to fix it fast.”

---

