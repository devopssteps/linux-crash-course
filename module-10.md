# 🎯 Linux Logs & Monitoring

## 🧠 Concept

Logs = records of what is happening in your system

👉 In DevOps, logs help you:
 - ✔ Debug errors
 - ✔ Monitor applications
 - ✔ Find root cause of failures

---

## 📂 Where Logs Are Stored

👉 Most logs are inside:

```bash id="logdir"
/var/log
```

---

# 💻 🧪 HANDS-ON DEMO

---

# 📁 STEP 1: Explore Log Directory

```bash id="lslog"
ls /var/log
```

👉 Common files:

* `syslog` → system logs
* `auth.log` → login/authentication
* `nginx/` → web server logs

---

> “Whenever something breaks, the first place a DevOps engineer checks is /var/log.”

---

# 📜 STEP 2: View Log Files

## 🔹 Show full content

```bash id="catlog"
cat /var/log/syslog
```

---

## 🔹 Better way (scrollable)

```bash id="lesslog"
less /var/log/syslog
```

👉 Press:

* `q` to exit

---

## 🔹 View last lines (MOST USED)

```bash id="taillog"
tail /var/log/syslog
```

---

## 🔥 Live monitoring (VERY IMPORTANT)

```bash id="tailf"
tail -f /var/log/syslog
```

👉 Shows logs in real-time

---

> “tail -f is one of the most powerful commands — it lets you watch logs live while your app is running.”

---

# 🔍 STEP 3: Search Logs (IMPORTANT)

```bash id="grep"
grep "error" /var/log/syslog
```

---

## 🔹 Case-insensitive search

```bash id="grep2"
grep -i "failed" /var/log/auth.log
```

---

# 📊 STEP 4: Monitor System Resources

## 🔹 CPU & Memory

```bash id="top"
top
```

---

## 🔹 Disk usage

```bash id="df"
df -h
```

---

## 🔹 Memory usage

```bash id="free"
free -m
```

---

# ⚙️ STEP 5: Service Logs (IMPORTANT)

## 🔹 Check service logs

```bash id="journal"
journalctl -u nginx
```

---

## 🔹 Live logs

```bash id="journalf"
journalctl -u nginx -f
```

---

# 🧠 DevOps Real-Life Scenarios (VERY IMPORTANT)

---

## 🔥 Scenario 1: Website not working

```bash id="real1"
tail -f /var/log/nginx/error.log
```

👉 Find error instantly

---

## 🔥 Scenario 2: Login issue

```bash id="real2"
cat /var/log/auth.log
```

---

## 🔥 Scenario 3: Application crash

```bash id="real3"
grep "error" /var/log/syslog
```

---

## 🔥 Scenario 4: High CPU

```bash id="real4"
top
```

👉 Identify process

---

# ⚠️ Important Tips

 - ✔ Always use `tail -f` for live debugging
 - ✔ Use `grep` to filter logs
 - ✔ Logs can grow very large → clean regularly

---

# 🧹 Clean Logs 

```bash id="cleanup"
sudo rm -rf /var/log/*.gz
```

---

# 🧠 Quick Summary

| Command     | Purpose           |
| ----------- | ----------------- |
| ls /var/log | list logs         |
| tail        | last lines        |
| tail -f     | live logs         |
| grep        | search logs       |
| journalctl  | service logs      |
| top         | system monitoring |

---

> “Logs are the first thing you check in any production issue — mastering this can make you a strong DevOps engineer.”

---

> “If you know how to read logs, you can debug any problem in Linux.”

---
> “Your app is down? Don’t panic — just check these logs and you’ll find the issue in minutes.”

---


