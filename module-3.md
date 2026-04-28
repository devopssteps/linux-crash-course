# 🔥 Linux File & Directory Management

## 🧠 Concept

As a DevOps engineer, you constantly:

* Create config files
* Copy deployment files
* Move logs/backups
* Delete unused data

👉 These 4 operations are used **daily**:
✔ Create
✔ Copy
✔ Move/Rename
✔ Delete

---

# 💻 🧪 HANDS-ON DEMO (Step-by-Step)

## 📁 Step 1: Create Files & Directories

### 🔹 Create a file

```bash id="createfile"
touch file1.txt
```

👉 Check:

```bash id="ls1"
ls
```

---

### 🔹 Create a directory

```bash id="createdir"
mkdir mydir
```

👉 Check:

```bash id="ls2"
ls
```

---

### 🔹 Create multiple files

```bash id="multifile"
touch file2.txt file3.txt
```

---

### 🔹 Create nested directory

```bash id="nesteddir"
mkdir -p project/app/logs
```

---

> “As a DevOps engineer, you create directories for applications, logs, and deployments.”

---

# 📂 Step 2: Copy Files & Directories

## 🔹 Copy file

```bash id="copyfile"
cp file1.txt mydir/
```

👉 Verify:

```bash id="ls3"
ls mydir
```

---

## 🔹 Copy and rename

```bash id="copyrename"
cp file1.txt mydir/file-new.txt
```

---

## 🔹 Copy directory 

```bash id="copydir"
cp -r mydir backupdir
```

👉 Explain:

* `-r` = recursive (needed for folders)

---

> “We use copy to create backups or duplicate configuration files.”

---

# 🔁 Step 3: Move & Rename Files

## 🔹 Move file

```bash id="movefile"
mv file2.txt mydir/
```

---

## 🔹 Rename file

```bash id="renamefile"
mv file3.txt newfile.txt
```

---

## 🔹 Move directory

```bash id="movedir"
mv mydir project/
```

---

> “The mv command is very powerful — it’s used for both moving and renaming.”

---

# ❌ Step 4: Delete Files & Directories

## 🔹 Delete file

```bash id="deletefile"
rm file1.txt
```

---

## 🔹 Delete multiple files

```bash id="deletemulti"
rm file2.txt file3.txt
```

---

## 🔹 Delete directory

```bash id="deletedir"
rm -r project
```

---

## 🔥 Force delete

```bash id="force"
rm -rf project
```

👉 Explain carefully:

* `-r` = recursive
* `-f` = force (no confirmation)

⚠️ Dangerous command

---

> “rm -rf is one of the most dangerous commands in Linux — always double-check before running it.”

---

# 🔍 Verify Changes

```bash id="verify"
ls
pwd
```

---

# 🧠 DevOps Real-Life Example 

👉 Example: Copy config file

```bash id="real1"
cp /etc/nginx/nginx.conf /etc/nginx/nginx.conf.bak
```

👉 Example: Move logs

```bash id="real2"
mv /var/log/app.log /backup/
```

👉 Example: Clean old files

```bash id="real3"
rm -rf /tmp/*
```

---

# ⚡ Tips

✔ Use `-r` for directories
✔ Always verify before delete
✔ Take backup before editing

---

> “If you master file and directory management, you can handle any Linux server like a pro — and this is daily work in DevOps.”

---

> “If you don’t know these 4 Linux commands, you can’t survive in DevOps — let me show you why.”

---
