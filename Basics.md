# 🐧 Linux Commands Cheat Sheet (Extended - 150+ Commands)

This markdown provides a deep, categorized reference of over 150 essential Linux commands with syntax and examples.

---

## 📁 1. File & Directory Commands

### `ls`, `ls -a`, `ls -l`, `ls -la`

List directory contents in various formats.

### `cd`, `cd ..`, `cd ~`, `cd -`

Change directory, up one level, home, or previous directory.

### `pwd`

Print working directory.

### `mkdir`, `mkdir -p`

Make directory, with optional parent creation.

### `rmdir`, `rm -r`, `rm -rf`, `rm -f`

Remove directories (empty or non-empty), force deletion.

### `cp`, `cp -r`

Copy files/directories recursively.

### `mv`

Move or rename files/directories.

### `touch`

Create empty files.

### `tree`

Show directory structure (install with `sudo apt install tree`).

### `basename`, `dirname`

Get filename or directory part of a path.

---

## 📄 2. File Viewing & Editing

### `cat`, `tac`

View file content. `tac` shows content in reverse.

### `less`, `more`

Paged viewing of large files.

### `head`, `tail`, `tail -f`

Show beginning or end of files. `tail -f` monitors logs.

### `nano`, `vim`, `vi`

Terminal text editors.

### `xargs`, `cut`, `awk`, `sed`

Text parsing tools.

### `stat`

File/directory information (permissions, timestamps).

---

## 🔍 3. Search & Locate

### `find`, `find -type`, `find -name`, `find -exec`

Locate files by name, type, or execute actions.

### `locate`, `updatedb`

Fast file searching (requires updated database).

### `grep`, `egrep`, `grep -r`, `grep -i`

Search file contents with patterns.

### `which`, `whereis`

Locate the binary or documentation for commands.

### `diff`, `cmp`

Compare files.

---

## 📚 4. Help & Docs

### `man`, `man -k`, `whatis`, `info`

Command manuals and help pages.

### `--help`

Quick syntax reference for any command.

---

## 🛠️ 5. Permissions & Ownership

### `chmod`, `chmod +x`, `chmod 755`

Change file permissions.

### `chown`, `chgrp`

Change ownership and group.

### `umask`

Set default permission for new files.

---

## 📊 6. System Monitoring

### `top`, `htop`, `atop`

Real-time system monitoring tools.

### `ps aux`, `ps -ef`

Show running processes.

### `uptime`, `w`

System uptime and user sessions.

### `free -h`, `vmstat`, `iostat`

Memory, CPU, and IO usage.

### `df -h`, `du -sh`

Disk usage (human-readable, summary).

### `watch`, `time`

Run command repeatedly or time its execution.

---

## 🌐 7. Networking

### `ip a`, `ip r`, `ifconfig`, `route`

Show IP, routes, interfaces.

### `ping`, `traceroute`, `mtr`

Network diagnostics.

### `netstat`, `ss -tulnp`

Socket/network connection details.

### `curl`, `wget`

Download or interact with URLs.

### `scp`, `rsync`

Copy over SSH; `rsync` for incremental sync.

### `dig`, `nslookup`, `host`

DNS resolution tools.

### `nmap`, `tcpdump`

Network scanner and packet sniffer.

---

## 🔐 8. User & Group Management

### `whoami`, `id`, `groups`

Get current user info.

### `adduser`, `useradd`, `passwd`, `usermod`

User creation and modification.

### `groupadd`, `groupdel`, `gpasswd`

Group management.

### `su`, `sudo`, `sudo -i`

Switch user or escalate privileges.

### `chage`, `last`, `who`, `w`

User login tracking and password aging.

---

## 🐾 9. Package Management (Debian/Ubuntu)

### `apt`, `apt-get`, `apt-cache`

Install, update, search packages.

```bash
sudo apt update && sudo apt upgrade
sudo apt install package-name
```

### `dpkg -i`, `dpkg -l`, `dpkg -r`

Low-level Debian package commands.

---

## 🛋️ 10. Disk & File System

### `lsblk`, `blkid`

List block devices.

### `fdisk`, `parted`, `gparted`

Partition tools.

### `mount`, `umount`

Mount or unmount devices.

### `mkfs`, `fsck`

Create/check file systems.

---

## 📦 11. Archive & Compression

### `tar`, `gzip`, `gunzip`, `zip`, `unzip`, `xz`

Compression utilities.

### `tar -cvf`, `tar -xvf`, `tar -czf`, `tar -xzf`

Archive, extract, compress.

---

## ⚙️ 12. System Boot & Services

### `systemctl`, `service`, `journalctl`

Systemd service manager and logs.

```bash
sudo systemctl start nginx
sudo systemctl status ssh
journalctl -xe
```

### `reboot`, `shutdown`, `halt`, `poweroff`

System power controls.

---

## 📝 13. Bash & Scripting

### `bash`, `sh`, `source`

Execute or load shell scripts.

### `echo`, `read`, `export`, `unset`

Environment and variable commands.

### `alias`, `unalias`

Command shortcuts.

### `&&`, `||`, `;`, `&`

Command chaining.

### `for`, `while`, `if`, `case`

Control structures in shell.

---

## 🔁 14. System Updates & Backups

### `cron`, `crontab`, `at`, `rsync`

Scheduling tasks and syncing files.

### `tar`, `rsync`, `scp`

Backup and remote sync.

---

## 🔒 15. Security & Permissions

### `ufw`, `iptables`

Firewall management.

### `gpg`, `openssl`

Encryption and certificates.

---

## 📂 16. Useful Utilities

### `watch`, `time`, `yes`, `tee`, `xargs`, `sort`, `uniq`

Monitoring and batch tools.

### `basename`, `dirname`, `file`, `wc`, `cut`, `split`

Text/file processing tools.

### `sleep`, `wait`, `bg`, `fg`, `jobs`, `kill`, `killall`

Process control.

---

This document includes over 150 commonly used Linux commands categorized by functionality.

> Tip: Combine commands using pipelines (`|`) and redirections (`>`, `>>`, `2>&1`) to build powerful scripts!
