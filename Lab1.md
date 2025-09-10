# Basic Linux Commands Cheat Sheet

This is a list of basic commands for the Linux terminal that are useful for everyday tasks.

## 📂 File System Navigation

Commands for moving around the file system.

| Command | Description | Example |
| ----- | ----- | ----- |
| `pwd` | **P**rint **W**orking **D**irectory (shows your current location). | `pwd` |
| `ls` | **L**i**s**t files and directories in the current location. | `ls -la` |
| `cd` | **C**hange **D**irectory. | `cd /home/user/documents` |
| `cd ..` | Go up one directory level. | `cd ..` |
| `cd ~` or `cd` | Go to your home directory. | `cd ~` |

## 📁 File & Directory Management

Commands for creating, deleting, and modifying files and directories.

| Command | Description | Example |
| ----- | ----- | ----- |
| `mkdir` | **M**a**k**e a new **dir**ectory. | `mkdir new_folder` |vgi
| `touch` | Create a new, empty file. | `touch new_file.txt` |
| `cp` | **C**o**p**y a file or directory. | `cp source.txt destination.txt` |
| `mv` | **M**o**v**e or rename a file or directory. | `mv old_name.txt new_name.txt` |
| `rm` | **R**e**m**ove a file. Use with caution! | `rm file_to_delete.txt` |
| `rm -r` | **R**emove a directory and its contents **r**ecursively. | `rm -r directory_to_delete` |

## ℹ️ System Commands

Commands to get information about your system.

| Command | Description | Example |
| ----- | ----- | ----- |
| `echo` | Usefull for debugginng or scripting. | `echo "heloo world"` |
| `whoami` | Displays the current user's username. | `whoami` |
| `man` | Useful for debugging or scripting.. | `man ls` |

## 🔍 Searching

Commands for finding files and text.

| Command | Description | Example |
| ----- | ----- | ----- |
| `find` | Search for files and directories. | `find /home -name "*.txt"` |
| `grep` | Search for a pattern of text within files. | `grep "hello" file.txt` |

![image](tet.png)

