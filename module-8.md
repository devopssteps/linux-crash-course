# 🎯 Linux Networking Commands

## 🧠 Concept (Simple + Real Meaning)

Networking commands help you:
 - ✔ Check IP address
 - ✔ Test connectivity
 - ✔ Debug server issues
 - ✔ Verify open ports

👉 In DevOps, this is used **daily** to troubleshoot production issues

---

# 💻 🧪 HANDS-ON DEMO (Step-by-Step)

---

# 🌐 STEP 1: Check IP Address

## 🔹 Command:

```bash id="ipa"
ip a
```

👉 Shows:

* IP address
* Network interface (eth0, ens33)

---

## 🔹 Short version:

```bash id="ipbrief"
ip -br a
```

---

> “This is how you check your server’s IP in real DevOps work.”

---

# 🌍 STEP 2: Check Internet Connectivity

## 🔹 Command:

```bash id="ping"
ping google.com
```

👉 Press:

```text id="ctrlc"
Ctrl + C
```

to stop

---

👉 If fail:

* Network issue
* DNS issue

---

# 🌍 STEP 3: Check Public IP

```bash id="publicip"
curl ifconfig.me
```

👉 Used in AWS security groups

---

# 🔍 STEP 4: Check Open Ports

## 🔹 Command:

```bash id="ss"
ss -tulnp
```

👉 Shows:

* Listening ports
* Services running

---

## 🔹 Alternative:

```bash id="netstat"
netstat -tulnp
```

---

> “If your app is not accessible, first check if the port is open.”

---

# 🌐 STEP 5: DNS Lookup

## 🔹 Command:

```bash id="nslookup"
nslookup google.com
```

---

## 🔹 Alternative:

```bash id="dig"
dig google.com
```

👉 Shows:

* DNS resolution

---

# 🔗 STEP 6: Test Web Server

```bash id="curltest"
curl http://localhost
```

---

👉 Test remote:

```bash id="curlremote"
curl http://your-server-ip
```

---

# 🧭 STEP 7: Trace Network Path

```bash id="trace"
traceroute google.com
```

👉 Shows:

* Path from your server → destination

---

# 🔌 STEP 8: Check Interface Details

```bash id="iplink"
ip link
```

---

# 🧠 DevOps Real-Life Scenarios 

---

## 🔥 Scenario 1: App not accessible

```bash id="real1"
ss -tulnp
```

👉 Check port running or not

---

## 🔥 Scenario 2: Server no internet

```bash id="real2"
ping 8.8.8.8
```

 - 👉 If works → DNS issue
 - 👉 If not → network issue

---

## 🔥 Scenario 3: Domain not working

```bash id="real3"
nslookup yourdomain.com
```

---

## 🔥 Scenario 4: API test

```bash id="real4"
curl http://api-server
```

---

# ⚠️ Important Tips

✔ Use `ss` instead of `netstat` (modern)
✔ Always check:

* IP
* Port
* Connectivity

---

# 🧠 Quick Summary

| Command    | Purpose           |
| ---------- | ----------------- |
| ip a       | check IP          |
| ping       | test connectivity |
| curl       | test API/web      |
| ss         | check ports       |
| nslookup   | DNS check         |
| traceroute | network path      |

---

> “Networking issues are the most common problems in DevOps — and these commands help you solve them quickly.”

---

> “If you master these networking commands, you can debug almost any server issue in minutes.”

---

> “If your server is not working, these 5 commands will save your job — let me show you.”

---

