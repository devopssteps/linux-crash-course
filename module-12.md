# 🎯 Linux Shell Basics

## 🧠 Concept 

👉 The **shell** is where you type commands and control Linux

* It acts as a bridge between **you ↔ operating system**
* Most common shell: **Bash (Bourne Again Shell)**

👉 As a DevOps engineer:
 - ✔ You automate tasks
 - ✔ Run scripts
 - ✔ Manage servers

---

# 💻 🧪 HANDS-ON DEMO

---

# 🖥️ STEP 1: Open Terminal

👉 In Linux / WSL:

* Open terminal

👉 You’ll see something like:

```bash id="prompt"
ubuntu@server:~$
```

👉 This is called **shell prompt**

---

# 🔍 STEP 2: Check Current Shell

```bash id="shell"
echo $SHELL
```

👉 Output:

```text id="shellout"
/bin/bash
```

---

# 📍 STEP 3: Check Current Directory

```bash id="pwd"
pwd
```

👉 Shows where you are

---

# 📂 STEP 4: List Files

```bash id="ls"
ls
```

---

## 🔹 Detailed list

```bash id="lsl"
ls -l
```

---

## 🔹 Show hidden files

```bash id="lsa"
ls -a
```

---

# 🔄 STEP 5: Navigate Directories

## 🔹 Go to folder

```bash id="cd"
cd /var/log
```

---

## 🔹 Go back

```bash id="cdback"
cd ..
```

---

## 🔹 Go home

```bash id="cdhome"
cd ~
```

---

# 🧠 STEP 6: Understand Commands Structure

👉 Basic format:

```bash id="format"
command [options] [arguments]
```

---

## 🔹 Example:

```bash id="example"
ls -l /var
```

* `ls` → command
* `-l` → option
* `/var` → argument

---

# ⌨️ STEP 7: Command History (VERY USEFUL)

```bash id="history"
history
```

---

## 🔹 Run previous command

```bash id="bang"
!5
```

---

## 🔹 Reverse search

```bash id="ctrlr"
Ctrl + R
```

---

# 🧩 STEP 8: Tab Completion (IMPORTANT)

👉 Type:

```bash id="tab"
cd /va
```

👉 Press **Tab** → auto-complete to `/var`

---

# 🔗 STEP 9: Command Chaining

## 🔹 Run multiple commands

```bash id="chain"
mkdir test && cd test && touch file.txt
```

---

👉 `&&` = run next only if previous success

---

# 🔁 STEP 10: Redirect Output (IMPORTANT)

## 🔹 Save output to file

```bash id="redirect"
ls > output.txt
```

---

## 🔹 Append

```bash id="append"
ls >> output.txt
```

---

# 🔄 STEP 11: Pipe Commands (VERY IMPORTANT)

```bash id="pipe"
ls -l | grep file
```

👉 Output of one command → input of another

---

# 🧠 DevOps Real-Life Examples

---

## 🔥 Example 1: Check logs

```bash id="real1"
cat /var/log/syslog | grep error
```

---

## 🔥 Example 2: Create project quickly

```bash id="real2"
mkdir app && cd app && touch app.py
```

---

## 🔥 Example 3: Save command output

```bash id="real3"
ps aux > process.txt
```

---

# ⚠️ Important Tips

 - ✔ Use **Tab** to save time
 - ✔ Use **history** to reuse commands
 - ✔ Use **pipes (|)** for powerful filtering

---

# 🧠 Quick Summary

| Command | Purpose           |             |
| ------- | ----------------- | ----------- |
| pwd     | current directory |             |
| ls      | list files        |             |
| cd      | change directory  |             |
| history | command history   |             |
|         |                   | pipe output |
| >       | redirect output   |             |

---

> “If you master the Linux shell, you can control any server faster than using any UI.”

---
> “The shell is the heart of DevOps — everything starts from here.”

---
> “If you don’t know Linux shell, you can’t become a DevOps engineer.”

---

