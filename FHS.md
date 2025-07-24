# 🏛️ Linux Filesystem Structure and Architecture (Very In-Depth)

## `/` – Root Directory

* Top-level directory from which all others branch.
* Owned by root.
* Not the same as `/root` (root user’s home).

---

## 🔹 `/bin` – Essential User Binaries

* Contains essential command-line tools for all users.
* Examples: `ls`, `cp`, `mv`, `cat`, `chmod`, `mkdir`

## 🔹 `/sbin` – System Binaries

* System-level utilities for superusers.
* Examples: `fsck`, `reboot`, `shutdown`, `ifconfig`

## 🔹 `/boot` – Boot Loader Files

* Holds files required to boot the system.
* Kernel, GRUB config, initrd images.
* Examples: `/boot/vmlinuz-*`, `/boot/initrd.img-*`, `/boot/grub/`

## 🔹 `/dev` – Device Files

* Interface to hardware devices.
* Managed by `udev`.
* Examples: `/dev/sda`, `/dev/null`, `/dev/tty`, `/dev/random`

## 🔹 `/etc` – Configuration Files

* System-wide config files.
* Examples: `/etc/passwd`, `/etc/hostname`, `/etc/fstab`, `/etc/systemd/`

## 🔹 `/home` – User Home Directories

* Personal directories for each user.
* Example: `/home/aravind/` with Documents, Downloads, etc.

## 🔹 `/lib`, `/lib64` – Shared Libraries

* Libraries required by binaries in `/bin` and `/sbin`.
* `.so` files (shared objects).

## 🔹 `/media` – Removable Media

* Auto-mounted USB, CD-ROM, etc.
* Example: `/media/usb`, `/media/cdrom`

## 🔹 `/mnt` – Manual Mount Point

* Used by admins for manual mounting.
* Example: `mount /dev/sdb1 /mnt`

## 🔹 `/opt` – Optional Software

* For third-party or proprietary apps.
* Example: `/opt/google/chrome/`

## 🔹 `/proc` – Process Info (Virtual FS)

* Interface to kernel and process info.
* Virtual filesystem (dynamic content).
* Examples: `/proc/cpuinfo`, `/proc/meminfo`, `/proc/<PID>/`

## 🔹 `/root` – Root User’s Home Directory

* Home of the root user.
* Not the same as `/`.

## 🔹 `/run` – Runtime Data

* Temporary runtime info (e.g., PID files).
* Exists in RAM (`tmpfs`).

## 🔹 `/srv` – Service Data

* Data for services like FTP or HTTP.
* Example: `/srv/www/`, `/srv/ftp/`

## 🔹 `/sys` – Kernel Interface (Virtual FS)

* Interface to kernel devices and modules.
* Examples: `/sys/class/net/`, `/sys/block/`

## 🔹 `/tmp` – Temporary Files

* Writable by all users.
* Cleared on reboot.
* Permissions usually `1777` (sticky bit).

## 🔹 `/usr` – Secondary Hierarchy

* User programs and libraries.
* Subdirs:

  * `/usr/bin` – User binaries
  * `/usr/sbin` – System binaries
  * `/usr/lib`, `/usr/include`, `/usr/local`

## 🔹 `/var` – Variable Data

* Data that changes frequently.
* Examples:

  * `/var/log/` – Logs
  * `/var/mail/` – User emails
  * `/var/cache/`, `/var/tmp/`

---

## 🔸 Hidden and Special Directories

* `.bashrc`, `.profile`, `.config/` – User settings
* `/lost+found` – Recovered files (ext4 fs)

---

## 🧠 Linux Admin Pro Tips

| Command                   | Purpose                  |
| ------------------------- | ------------------------ |
| `tree /`                  | Visual hierarchy         |
| `ls -l /`                 | Permissions and owners   |
| `du -sh /var/*`           | Disk usage in `/var`     |
| `mount`, `df -h`, `lsblk` | Disk and mount info      |
| `chmod`, `chown`          | File access control      |
| `systemctl`, `journalctl` | Manage services and logs |

---

> 📌 This layout is based on the Linux Filesystem Hierarchy Standard (FHS). Knowing it is essential for troubleshooting, configuring, and securing Linux systems.
