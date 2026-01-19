# Essential Terminal Commands Every Developer Should Know

This document is a practical, developer-focused reference of commonly used terminal (Unix/Linux/macOS) commands, grouped by category, with clear explanations and examples.

---

## 1. Navigation & File System

### `pwd`

Prints the current working directory.

```bash
pwd
```

### `ls`

Lists files and directories.

```bash
ls
ls -l
ls -a
ls -lh
```

### `cd`

Changes the current directory.

```bash
cd folder
cd ..
cd ~
cd -
```

### `tree`

Displays directory structure as a tree.

```bash
tree
tree -L 2
```

---

## 2. File & Directory Management

### `touch`

Creates an empty file.

```bash
touch file.txt
```

### `mkdir`

Creates directories.

```bash
mkdir folder
mkdir -p a/b/c
```

### `cp`

Copies files or directories.

```bash
cp src.txt dest.txt
cp -r src_dir dest_dir
```

### `mv`

Moves or renames files/directories.

```bash
mv old.txt new.txt
mv file.txt folder/
```

### `rm`

Deletes files or directories.

```bash
rm file.txt
rm -r folder
rm -rf folder
```

### `stat`

Shows detailed file information.

```bash
stat file.txt
```

---

## 3. Viewing & Editing Files

### `cat`

Displays file content.

```bash
cat file.txt
```

### `less`

Scrolls through file content.

```bash
less file.txt
```

### `head` / `tail`

Displays the first or last lines of a file.

```bash
head file.txt
tail file.txt
tail -f logs.txt
```

### `nano` / `vim`

Terminal-based text editors.

```bash
nano file.txt
vim file.txt
```

---

## 4. Search & Text Processing

### `grep`

Searches text using patterns.

```bash
grep "error" file.txt
grep -r "TODO" .
```

### `find`

Searches for files and directories.

```bash
find . -name "*.py"
find /var -size +100M
```

### `wc`

Counts lines, words, and characters.

```bash
wc file.txt
wc -l file.txt
```

### `sort`

Sorts lines in a file.

```bash
sort file.txt
sort -n numbers.txt
```

### `uniq`

Removes duplicate lines.

```bash
uniq file.txt
uniq -c file.txt
```

### `cut`

Extracts columns from text.

```bash
cut -d"," -f1 file.csv
```

### `awk`

Pattern scanning and text processing.

```bash
awk '{print $1}' file.txt
```

### `sed`

Stream editor for find/replace.

```bash
sed 's/foo/bar/g' file.txt
```

---

## 5. Permissions & Ownership

### `chmod`

Changes file permissions.

```bash
chmod 755 script.sh
chmod +x script.sh
```

### `chown`

Changes file owner and group.

```bash
chown user:group file.txt
```

### `umask`

Sets default permission mask.

```bash
umask
```

---

## 6. Process & System Management

### `ps`

Displays running processes.

```bash
ps aux
```

### `top` / `htop`

Real-time process monitoring.

```bash
top
htop
```

### `kill`

Terminates processes.

```bash
kill PID
kill -9 PID
```

### `jobs`, `bg`, `fg`

Manages background jobs.

```bash
jobs
bg %1
fg %1
```

### `uptime`

Shows system running time.

```bash
uptime
```

---

## 7. Disk & Memory

### `df`

Displays disk space usage.

```bash
df -h
```

### `du`

Displays directory size.

```bash
du -sh folder
```

### `free`

Shows memory usage.

```bash
free -h
```

---

## 8. Networking

### `curl`

Transfers data from URLs.

```bash
curl https://example.com
```

### `wget`

Downloads files.

```bash
wget https://example.com/file.zip
```

### `ping`

Checks network connectivity.

```bash
ping google.com
```

### `netstat` / `ss`

Displays network connections.

```bash
ss -tulpn
```

---

## 9. Archives & Compression

### `tar`

Creates and extracts archives.

```bash
tar -cvf file.tar folder
tar -xvf file.tar
```

### `gzip` / `gunzip`

Compresses and decompresses files.

```bash
gzip file.txt
gunzip file.txt.gz
```

### `zip` / `unzip`

Zip file operations.

```bash
zip file.zip file.txt
unzip file.zip
```

---

## 10. Environment & Shell

### `echo`

Prints text or variables.

```bash
echo "Hello"
echo $PATH
```

### `export`

Sets environment variables.

```bash
export NODE_ENV=production
```

### `env`

Lists environment variables.

```bash
env
```

### `alias`

Creates command shortcuts.

```bash
alias ll='ls -la'
```

### `history`

Shows command history.

```bash
history
```

---

## 11. Package Managers (Common)

### `apt` (Debian/Ubuntu)

```bash
sudo apt update
sudo apt install git
```

### `brew` (macOS)

```bash
brew install node
```

### `yum` / `dnf` (RHEL/Fedora)

```bash
sudo dnf install git
```

---

## 12. Git (Essential Developer Commands)

### `git clone`

Copies a remote repository.

```bash
git clone url
```

### `git status`

Shows working tree status.

```bash
git status
```

### `git add`

Stages changes.

```bash
git add .
```

### `git commit`

Commits staged changes.

```bash
git commit -m "message"
```

### `git pull` / `git push`

Syncs with remote repository.

```bash
git pull
git push
```

### `git log`

Shows commit history.

```bash
git log --oneline
```

---

## 13. Power User Shortcuts

* `Ctrl + C` → Stop process
* `Ctrl + Z` → Suspend process
* `Ctrl + R` → Reverse search history
* `!!` → Run previous command
* `!n` → Run command number `n`

---

## 14. Redirection & Pipes

### Output Redirection

```bash
command > file.txt
command >> file.txt
```

### Input Redirection

```bash
command < file.txt
```

### Pipes

```bash
command1 | command2
```

---

## 15. Useful One-Liners

```bash
# Find largest files
find . -type f -exec du -h {} + | sort -rh | head

# Kill process by name
pkill process_name

# Count occurrences
sort file.txt | uniq -c
```

---

## Final Notes

* These commands work on **Linux and macOS** (most also work in WSL).
* Mastering piping and text tools (`grep`, `awk`, `sed`) significantly boosts productivity.
* Keep this file bookmarked or printed for daily use.

Happy hacking 
