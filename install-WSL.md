# Install WSL (Windows Subsystem for Linux) on Windows 10/11

WSL allows you to run Linux directly inside Windows without a virtual machine.

## Step 1: Check Your Windows Version

Open **Run**:

```text
Win + R
```

Type:

```text
winver
```

For the easiest installation, you should have:

* Windows 10 Version 2004 or later
* Build 19041 or later

---

## Step 2: Open PowerShell as Administrator

Click:

```text
Start Menu
```

Search:

```text
PowerShell
```

Right-click:

```text
Run as Administrator
```

---

## Step 3: Install WSL

Run:

```powershell
wsl --install
```
If any sepecfic version you want to install then Run:

```sh
 wsl --install -d Ubuntu-22.04
```

This command automatically:

* Enables WSL
* Installs WSL2
* Installs Virtual Machine Platform
* Downloads Ubuntu
* Sets WSL2 as default

---

## Step 4: Restart Windows

After installation:

```text
Restart your computer
```

---

## Step 5: Complete Ubuntu Setup

After reboot, Ubuntu will open automatically.

Create:

```text
Username:
```

Example:

```text
rajiv
```

Create:

```text
Password:
```

Example:

```text
MyPassword123
```

You now have a Linux terminal.

---
# check which version is isntalled chech from bash 
```sh
lsb_release -a
```

# Verify Installation - form powershell 

Open PowerShell:

```powershell
wsl -l -v
```

Example output:

```text
NAME      STATE      VERSION
Ubuntu    Running    2
```

Version should be:

```text
2
```

---
# Downgrade to WSL 1
```sh
Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform
```
Restart computer 

### Force WSL to default to Version 1:
```sh
wsl --set-default-version 1
```
### Now install ubuntu 
```sh
wsl --install -d Ubuntu-22.04
```
---
# Install a Different Linux Distribution

View available distributions:

```powershell
wsl --list --online
```

Example output:

```text
Ubuntu
Debian
Kali-Linux
Ubuntu-22.04
Ubuntu-24.04
```

Install Ubuntu 24.04:

```powershell
wsl --install -d Ubuntu-24.04
```

Install Debian:

```powershell
wsl --install -d Debian
```

---
## Install WSL we follow the following setps
```sh
Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform
wsl --set-default-version 2
wsl --install -d Ubuntu-22.04
```
---
# Check WSL Status

```powershell
wsl --status
```

Example:

```text
Default Version: 2
```
