
# 🔍 Linux `find` Command Cheat Sheet for Security Researchers

As a security researcher, you’ll often need to locate files or folders on a system using various filters such as filename, size, user, group, and dates. This guide provides a concise cheat sheet with real examples.

---

## 📁 Find by Filename

```bash
find [directory path] -type f -name [filename]
```

**Example**:
```bash
find /home/Andy -type f -name sales.txt
```

---

## 📂 Find by Directory Name

```bash
find [directory path] -type d -name [directory name]
```

**Example**:
```bash
find /home/Andy -type d -name pictures
```

---

## 📏 Find by Size

```bash
find [directory path] -type f -size [size]
```

**Example**:
```bash
find /home/Andy -type f -size 10c
```

**Size Suffixes**:
- `c` = bytes  
- `k` = kilobytes  
- `M` = megabytes  
- `G` = gigabytes  

---

## 👤 Find by Username

```bash
find [directory path] -type f -user [username]
```

**Example**:
```bash
find /etc/server -type f -user john
```

---

## 👥 Find by Group Name

```bash
find [directory path] -type f -group [group name]
```

**Example**:
```bash
find /etc/server -type f -group teamstar
```

---

## 📅 Find Files Modified After a Specific Date

```bash
find [directory path] -type f -newermt '[date and time]'
```

**Example**:
```bash
find / -type f -newermt '6/30/2020 0:00:00'
```

---

## 📆 Find by Date Modified Range

```bash
find [directory path] -type f -newermt [start date] ! -newermt [end date]
```

**Example**:
```bash
find / -type f -newermt 2013-09-12 ! -newermt 2013-09-14
```

(Finds files modified **on 2013-09-13**)

---

## ⏳ Find by Date Accessed Range

```bash
find [directory path] -type f -newerat [start date] ! -newerat [end date]
```

**Example**:
```bash
find / -type f -newerat 2017-09-12 ! -newerat 2017-09-14
```

(Finds files accessed **on 2017-09-13**)

---

## 🔑 Find Files with Specific Keyword (Content)

```bash
grep -iRl [keyword] [directory path]
```

**Example**:
```bash
grep -iRl flag /folderA/
```

---

## 📘 Extra Tips

- Use `man find` to explore all available options.
- Visit [https://explainshell.com](https://explainshell.com) to break down complex command syntax.
- Add `2>/dev/null` at the end of a command to suppress permission errors:
  ```bash
  find / -type f -name "*.conf" 2>/dev/null
  ```
- Press `CTRL+L` to clear the terminal screen.
- Use the ↑ arrow to navigate through your command history.

---

Happy Hunting! 🕵️‍♂️
