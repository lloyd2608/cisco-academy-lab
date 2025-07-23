# 📑 Lab - Reading Server Logs (Cisco CyberOps)

## 🧾 Description
In this lab, I explored how to read and interpret server log files using various Linux tools. The lab focused on using commands like `cat`, `more`, `less`, and `journalctl` to view and navigate system logs. I also gained an understanding of how Syslog works and where key log files are stored in Linux systems. All exercises were completed in a safe, educational environment.

---

## 📋 Lab Objectives

- Reading log files using `cat`, `more`, and `less`
- Understanding the role of **Syslog** in Linux
- Viewing logs using `journalctl`

---

## 🧠 Skills Demonstrated

- Navigating large log files efficiently
- Interpreting system events through logs
- Using terminal-based tools to analyze logs
- Differentiating between logs stored in `/var/log/` and logs managed by `systemd`

---

## 🛠️ Tools & Commands Used

- `cat` – quick view of file contents
- `more` – scroll through logs page by page
- `less` – advanced navigation and search in logs
- `journalctl` – view logs from `systemd` services
- `/var/log/syslog`, `/var/log/auth.log`, and other system log files

---

## 📌 Example Commands Used

cat /var/log/syslog
more /var/log/auth.log
less /var/log/dmesg
journalctl -xe

