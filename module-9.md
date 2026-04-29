# 🎯 Linux Disk Management

## 🧠 Concept (Simple + Real Meaning)

Disk management = how you:
 - ✔ Check disk space
 - ✔ Monitor usage
 - ✔ Attach new storage (EBS in cloud)
 - ✔ Mount disks
 - ✔ Prevent “disk full” issues

👉 In DevOps, this is **critical** because:

* Apps fail when disk is full
* Logs grow fast
* Databases need storage

---

# 💻 🧪 HANDS-ON DEMO

---

# 📊 STEP 1: Check Disk Space

## 🔹 Command:

```bash id="df"
df -h
```

👉 Shows:

* Total space
* Used space
* Available space

👉 `-h` = human readable

---

> “This is the first command you run when your server is down due to disk issues.”

---

# 📁 STEP 2: Check Directory Size

```bash id="du"
du -sh *
```

👉 Shows size of each folder

---

## 🔥 Find largest directory

```bash id="duvar"
du -sh /var/*
```

👉 Useful for logs

---

# 🧱 STEP 3: List Disks & Partitions

```bash id="lsblk"
lsblk
```

👉 Shows:

* Disk name (e.g., nvme0n1)
* Partitions

---

## 🔹 More details:

```bash id="fdisk"
sudo fdisk -l
```

---

# 🆕 STEP 4: Add New Disk (Cloud Example)

👉 Example: AWS EBS or Azure Disk

---

## 🔍 Check new disk

```bash id="newdisk"
lsblk
```

👉 Example:

```text id="diskout"
nvme0n1
nvme1n1  <-- new disk
```

---

# 🧩 STEP 5: Create Partition

```bash id="partition"
sudo fdisk /dev/nvme1n1
```

👉 Steps:

* `n` → new partition
* `w` → write changes

---

# 🧾 STEP 6: Format Disk

👉 For XFS (common in cloud):

```bash id="format"
sudo mkfs.xfs /dev/nvme1n1p1
```

---

# 📂 STEP 7: Mount Disk

## 🔹 Create mount point

```bash id="mkdir"
sudo mkdir /data
```

---

## 🔹 Mount

```bash id="mount"
sudo mount /dev/nvme1n1p1 /data
```

---

## 🔍 Verify

```bash id="dfcheck"
df -h
```

---

# 🔁 STEP 8: Permanent Mount (IMPORTANT)

Edit:

```bash id="fstab"
sudo nano /etc/fstab
```

👉 Add:

```text id="fstabline"
/dev/nvme1n1p1 /data xfs defaults 0 0
```

---

# 🧠 DevOps Real-Life Scenarios

---

## 🔥 Scenario 1: Disk full issue

```bash id="real1"
df -h
```

👉 Then:

```bash id="real2"
du -sh /var/log/*
```

👉 Find large logs

---

## 🔥 Scenario 2: Clean logs

```bash id="real3"
sudo rm -rf /var/log/*.gz
```

---

## 🔥 Scenario 3: Attach new disk

 - ✔ Create partition
 - ✔ Format
 - ✔ Mount

---

## 🔥 Scenario 4: Extend disk (XFS)

```bash id="real4"
sudo xfs_growfs /
```

---

# ⚠️ Important Tips

 - ✔ Always check disk before deploy
 - ✔ Monitor `/var/log`
 - ✔ Use separate disk for data

---

# 🧠 Quick Summary

| Command | Purpose           |
| ------- | ----------------- |
| df -h   | check disk space  |
| du -sh  | check folder size |
| lsblk   | list disks        |
| fdisk   | partition disk    |
| mkfs    | format disk       |
| mount   | attach disk       |

---

> “Disk issues are one of the most common production problems — and these commands help you solve them fast.”

---

> “If you master disk management, you can handle scaling and storage issues like a real DevOps engineer.”

---

> “If your server shows ‘disk full’, these commands will save your system — let me show you.”

---

