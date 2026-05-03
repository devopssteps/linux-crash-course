
# 🎯 Linux File System Structure (Important Directories)

👉 Everything starts from:

```bash
/
```

This is called the **root directory**

---

# 📂 🔥 Core Directories Explained

---

## 📁 `/bin` (Essential User Binaries)

👉 Basic commands required for system boot & minimal usage

✔ Contains:

* `ls`
* `cp`
* `mv`
* `cat`

👉 Used by all users

---

## 📁 `/sbin` (System Binaries)

👉 System/admin commands

✔ Contains:

* `fdisk`
* `reboot`
* `ifconfig`

👉 Mostly used by root/admin

---

## 📁 `/etc` (Configuration Files)

👉 System-wide configuration

✔ Contains:

* `/etc/passwd`
* `/etc/ssh/sshd_config`
* `/etc/nginx/nginx.conf`

👉 Very important for DevOps

---

## 📁 `/home` (User Home Directory)

👉 Personal files of users

✔ Example:

```bash
/home/ubuntu
```

---

## 📁 `/root` (Root User Home)

👉 Home directory of root user

---

## 📁 `/var` (Variable Data)

👉 Data that changes frequently

✔ Contains:

* Logs → `/var/log`
* Web files → `/var/www`
* Cache → `/var/cache`

👉 Very important for troubleshooting

---

## 📁 `/tmp` (Temporary Files)

👉 Temporary files

✔ Automatically cleaned sometimes

---

## 📁 `/usr` (User Programs & Libraries)

👉 Secondary programs and utilities

✔ Contains:

* `/usr/bin` → normal commands
* `/usr/sbin` → admin commands
* `/usr/lib` → libraries

---

## 📁 `/lib` and `/lib64` (Libraries)

👉 Essential libraries for `/bin` and `/sbin`

---

## 📁 `/boot` (Boot Files)

👉 Files needed to boot system

✔ Contains:

* Kernel
* Bootloader (GRUB)

---

## 📁 `/dev` (Device Files)

👉 Represents hardware devices

✔ Examples:

* `/dev/sda`
* `/dev/nvme0n1`

---

## 📁 `/proc` (Process Info – Virtual)

👉 Runtime system info

✔ Examples:

* `/proc/cpuinfo`
* `/proc/meminfo`

---

## 📁 `/sys` (System Info – Virtual)

👉 Kernel and hardware info

---

## 📁 `/mnt` (Temporary Mount)

👉 Used to mount external storage manually

---

## 📁 `/media` (Removable Devices)

👉 USB, CD-ROM auto mount

---

## 📁 `/opt` (Optional Software)

👉 Third-party applications

---

## 📁 `/srv` (Service Data)

👉 Data for services

---

# 🧠 DevOps Quick Mapping (VERY IMPORTANT)

| Directory  | Used For           |
| ---------- | ------------------ |
| `/etc`     | Config files       |
| `/var/log` | Logs               |
| `/var/www` | Web apps           |
| `/home`    | User data          |
| `/usr/bin` | Installed programs |
| `/tmp`     | Temp files         |
| `/dev`     | Disks/devices      |

---

# 💻 🧪 HANDS-ON DEMO COMMANDS

---

## 🔍 List root structure

```bash
ls /
```

---

## 📂 Explore important folders

```bash
cd /etc
ls
```

```bash
cd /var/log
ls
```

---

## 🔍 Check binaries

```bash
ls /bin
```

---

## 🔍 Check device files

```bash
ls /dev
```

---

## 🔍 Check system info

```bash
cat /proc/cpuinfo
```

---

> “If you understand where everything is stored in Linux, you can troubleshoot any issue much faster as a DevOps engineer.”

---

> “Linux file system is like a map — once you know it, you’ll never feel lost in any server.”

---

# 🚀 Pro Tip (VERY IMPORTANT)

👉 Most used paths in DevOps:

* `/etc` → config
* `/var/log` → logs
* `/var/www` → web apps

---


