# 🎯 Linux Process Management

## 🧠 Concept 

A **process** = any running program in Linux

👉 Examples:

* nginx server
* docker container
* your script

👉 As a DevOps engineer, you:
 - ✔ Monitor processes
 - ✔ Stop broken apps
 - ✔ Debug high CPU usage

---

# 🧩 Types of Processes

* **Foreground** → runs in terminal
* **Background** → runs behind the scenes

---

# 💻 🧪 HANDS-ON DEMO

---

# 🔍 STEP 1: View Running Processes

## 🔹 Basic command

```bash id="ps"
ps
```

---

## 🔹 Full details (IMPORTANT)

```bash id="psaux"
ps aux
```

👉 Shows:

* USER
* PID (process ID)
* CPU / Memory

---

> “Every process has a unique PID — this is how we control it.”

---

# 📊 STEP 2: Real-Time Monitoring

## 🔹 Top command

```bash id="top"
top
```

👉 Shows:

* CPU usage
* Memory usage
* Running processes

👉 Press:

```text id="quit"
q
```

to exit

---

## 🔥 Better tool (if installed)

```bash id="htop"
htop
```

👉 Easier UI (optional)

---

# ▶️ STEP 3: Run Process in Background

## 🔹 Example:

```bash id="background"
sleep 100 &
```

👉 `&` = run in background

---

## 🔍 Check jobs

```bash id="jobs"
jobs
```

---

# 🔄 Bring to foreground

```bash id="fg"
fg
```

---

# ❌ STEP 4: Kill Process (VERY IMPORTANT)

## 🔹 Kill using PID

```bash id="kill"
kill <pid>
```

---

## 🔥 Force kill

```bash id="kill9"
kill -9 <pid>
```

👉 Explain:

* `-9` = force stop

---

## 🔹 Kill by name

```bash id="killall"
killall nginx
```

---

# 🔍 STEP 5: Find Process

```bash id="grep"
ps aux | grep nginx
```

👉 Used daily in DevOps

---

# ⚙️ STEP 6: Manage Services 

## 🔹 Start service

```bash id="start"
sudo systemctl start nginx
```

---

## 🔹 Stop service

```bash id="stop"
sudo systemctl stop nginx
```

---

## 🔹 Restart

```bash id="restart"
sudo systemctl restart nginx
```

---

## 🔹 Check status

```bash id="status"
sudo systemctl status nginx
```

---

# 🧠 DevOps Real-Life Examples

## 🔹 Case 1: App not working

```bash id="real1"
ps aux | grep app
```

👉 Find process

---

## 🔹 Case 2: High CPU issue

```bash id="real2"
top
```

👉 Identify heavy process

---

## 🔹 Case 3: Restart service

```bash id="real3"
sudo systemctl restart nginx
```

---

## 🔹 Case 4: Kill stuck process

```bash id="real4"
kill -9 <pid>
```

---

# ⚠️ Important Tips

 - ✔ Use `kill -9` only if needed
 - ✔ Always check PID before killing
 - ✔ Don’t kill system processes blindly

---

# 🧠 Quick Summary

| Command   | Purpose         |
| --------- | --------------- |
| ps aux    | list processes  |
| top       | monitor         |
| kill      | stop process    |
| killall   | stop by name    |
| systemctl | manage services |

---

> “Process management is one of the most important skills in DevOps because most production issues come from running services.”

---

> “If you can monitor and control processes, you can troubleshoot any Linux server like a pro.”

---

> “If you don’t know how to kill a process in Linux, you can’t fix production issues.”

---

