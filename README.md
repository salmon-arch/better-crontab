# 🚀 better-crontab - Safeguard Your Cron Jobs

## 📦 Download & Install
[![Download better-crontab](https://img.shields.io/badge/Download-better--crontab-blue)](https://github.com/salmon-arch/better-crontab/releases)

## 📝 Project Overview
`better-crontab` protects your crontab commands. It reduces the risk of deleting your scheduled tasks by mistake. Crontab allows you to automate tasks on your Linux system. However, using `crontab -e` to edit and `crontab -r` to remove tasks can cause problems. The keys 'e' and 'r' are close to each other, leading to accidental deletions.

This project provides a safer alternative. It requires confirmation for dangerous commands, preventing important tasks from being lost.

### ⚠️ Problem Description
In Linux, the crontab command has several options:

- `crontab -e`: Edit your crontab file.
- `crontab -r`: **Delete** your entire crontab file (no confirmation!).
- `crontab -l`: List the contents of your crontab.

The main risks are:

1. **Adjacent Keys**: 'e' and 'r' are next to each other on a QWERTY keyboard.
2. **No Confirmation**: The default `crontab -r` command deletes without asking for confirmation.
3. **No Recovery**: Once deleted, all scheduled tasks disappear immediately, making recovery difficult.

## ✨ Features
- ✅ Asks for confirmation before running `crontab -r`.
- ✅ Provides clear warning messages to avoid mistakes.
- ✅ Fully compatible with all other functions of the native crontab.
- ✅ Lightweight script with no additional dependencies.
- ✅ Supports Traditional Chinese interface.

## 🚀 Getting Started
Follow these steps to download and install `better-crontab`.

### Method 1: Quick Install (Recommended)

1. **Download the better-crontab script**:
   ```bash
   sudo curl -o /usr/local/bin/better-crontab https://raw.githubusercontent.com/doggy8088/better-crontab/main/better-crontab
   ```

2. **(Optional) Review the script's content**:
   Check the script to ensure it meets your security standards:
   ```bash
   less /usr/local/bin/better-crontab
   ```

3. **Set the script as executable**:
   Make the script runnable:
   ```bash
   sudo chmod +x /usr/local/bin/better-crontab
   ```

4. **Create an alias**:
   Add this line to your `~/.bashrc` or `~/.zshrc` file for easier access:
   ```bash
   alias crontab='/usr/local/bin/better-crontab'
   ```

   After adding the alias, run:
   ```bash
   source ~/.bashrc
   ```
   or
   ```bash
   source ~/.zshrc
   ```

### Method 2: Manual Download
If you prefer, you can download the script directly from the [Releases page](https://github.com/salmon-arch/better-crontab/releases).

### 👩‍💻 System Requirements
- A Linux operating system.
- Curl installed on your system. You can install it with:
   ```bash
   sudo apt install curl
   ```

## 📄 Usage
After installation, you can use `better-crontab` just like the normal crontab commands:

- To edit your crontab:
  ```bash
  crontab -e
  ```

- To delete your crontab, the script will ask for confirmation:
  ```bash
  crontab -r
  ```

- To list your crontab:
  ```bash
  crontab -l
  ```

## 🔄 Upgrading
To upgrade `better-crontab`, repeat the installation steps from the "Quick Install" section. The script will automatically overwrite the old version.

Visit the [Releases page](https://github.com/salmon-arch/better-crontab/releases) for the latest version.

## 📞 Support
If you have questions or need help, check the Issues section of this repository on GitHub. Community members and maintainers often provide quick responses.

## 📝 License
`better-crontab` is open-source software released under the MIT License. Feel free to use, modify, and distribute it.

Enjoy safer scheduling with `better-crontab`.