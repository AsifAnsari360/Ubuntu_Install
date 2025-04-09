# 🐧 Ubuntu 24.04 WSL Manual Setup Guide (Windows)

This guide helps you install and run **Ubuntu 24.04** on **Windows Subsystem for Linux (WSL)** using the official `.gz` root filesystem archive.

---

## ✅ Requirements

- Windows 10 version 2004 or later, or Windows 11
- Virtualization enabled in BIOS (Intel VT-x or AMD-V)
- [7-Zip](https://www.7-zip.org/download.html) installed for extracting `.gz` files

---

## 📥 Step 1: Download Ubuntu Root Filesystem

Download the file named `ubuntu-24.04.2-wsl-amd64.gz` from the official Ubuntu WSL image repository:
- https://cloud-images.ubuntu.com/wsl/

---

## 📂 Step 2: Extract the `.gz` File

1. Right-click the `ubuntu-24.04.2-wsl-amd64.gz` file.
2. Select ➜ `7-Zip` ➜ `Extract Here`.
3. You will get a file named `ubuntu-24.04.2-wsl-amd64` (with no extension).

---

## 📝 Step 3: Rename the File

Rename the extracted file to add a `.tar` extension:

> This is necessary because WSL requires the `.tar` format to import the distribution.

---

## 📁 Step 4: Create a WSL Directory

Open PowerShell and run:
```powershell```
mkdir D:\WSL\Ubuntu-24.04

# Move the .tar file into this new folder:

D:\WSL\Ubuntu-24.04\ubuntu-24.04.2-wsl-amd64.tar

## ⚙️ Step 5: Import Ubuntu into WSL

Open Command Prompt as Administrator and run:

`wsl --import Ubuntu-24.04 D:\WSL\Ubuntu-24.04 D:\WSL\Ubuntu-24.04\ubuntu-24.04.2-wsl-amd64.tar`

## 🚀 Step 6: Launch Ubuntu

`wsl -d Ubuntu-24.04` or `wsl.exe -d Ubuntu`

## 🛠️ Troubleshooting: HCS_E_SERVICE_NOT_AVAILABLE Error

Open PowerShell as Administrator and run:

`wsl --install` --> Launch `wsl.exe -d Ubuntu`

## 👤 Step 7: Create a User in Ubuntu

`adduser yourname`
`usermod -aG sudo yourname`

Then you can log in as that user:

`wsl -d Ubuntu-24.04 -u yourname` or `wsl.exe -d Ubuntu -u yourname`


### Thank You
