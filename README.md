# Linux-command-cheat-sheet2
# Mastering Linux Commands with Examples

This repository provides a comprehensive guide to using Linux commands, with examples and screenshots for clarity.

## Table of Contents
1. [User and Terminal Details](#1-user-and-terminal-details)
2. [File Operations](#2-file-operations)
   - Creating, Viewing, and Appending
3. [Word Count and Line Count](#3-word-count-line-count)
4. [Head and Tail Commands](#4-head-and-tail-commands)
5. [Linux Command-Line Shortcuts](#5-linux-command-line-shortcuts)
6. [Linux File System Hierarchy](#6-linux-file-system-hierachy)
7. [Move Command](#7-move-command)
8. [Copy Command](#8-copy-command)
9. [TTY and Virtual Terminals](#9-tty-and-vartual-terminals)
10. [Getting Command Information](#10-getting-command-information)
11. [Editing with Vim](#11-editing-with-vim)

---

### 1. User and Terminal Details
To display the current user and terminal details:

![Screenshot from 2024-11-28 17-11-45](https://github.com/user-attachments/assets/b11c50cc-3afb-4e0f-8f6a-1c87731b845c)


### 2. File Operations
Create a file and append to it:
- cat > f1
   - Purpose: Creates or overwrites the file f1.
   - Behavior:
      If f1 exists, its content will be erased, and new input will replace it.
      If f1 does not exist, it creates a new file.
   - Use Case: Start fresh with a new file or replace existing content.

![image](https://github.com/user-attachments/assets/5f8e4dca-2c67-4b49-a14e-9d32a354b9ad)

- cat >> f1
   - Purpose: Appends new content to the end of the file f1.
   - Behavior:
      If f1 exists, new input will be added to the end of the file without erasing the previous content.
      If f1 does not exist, it creates a new file.
   - Use Case: Add more content to an existing file without deleting its current data.

![image](https://github.com/user-attachments/assets/7086bc1d-bdd0-45e0-a7a0-05936c22d56a)

View file content:
- cat f1
- less f1
- gedit f1    # like notepad
- evince f1   # Open PDF file


### 3. Word Count (wc) Command
Display line, word, and character count of a file:

![Screenshot from 2024-11-28 17-50-15](https://github.com/user-attachments/assets/840608fb-29b7-4c48-a3c8-57b8be254f61)

6: Number of lines

7: Number of words

33: Number of characters

Commands for specific counts:
- Lines: wc -l f1
- Words: wc -w f1
- Characters: wc -c f1

![Screenshot from 2024-11-28 17-52-47](https://github.com/user-attachments/assets/3c6cb631-54a5-439e-9fe4-287df8022465)

### 4. Head and Tail Commands
Display first/last lines of a file:
- head

![Screenshot from 2024-11-28 17-55-46](https://github.com/user-attachments/assets/6c07b64f-38dd-4bd1-99e9-734fc524b703)

- tail

![Screenshot from 2024-11-28 17-57-07](https://github.com/user-attachments/assets/f857f9ec-ed41-4e33-9670-072133d59637)

### 5. Linux Command-Line Shortcuts
**Key shortcuts for efficient command-line use:**
- **Ctrl + A**: Move to the beginning of the line
- **Ctrl + E**: Move to the end of the line
- **Ctrl + R**: Search through command history
- **Ctrl + U**: Clear the current line
- **Ctrl + L**: Clear the screen

### 6. Linux File System Hierarchy
The Linux File System Hierarchy is an organized structure of directories and files that follows a standard layout, making it easy to navigate and manage. Here’s an overview of the main directories:

![Screenshot from 2024-11-28 18-09-12](https://github.com/user-attachments/assets/c9fe0a94-3bf2-4b2c-9d3a-4d7468bb47ce)

- **Root Directory:** /
The base of the Linux file system. All other directories and files stem from this root directory.

- **Key Directories in Linux**

![Screenshot from 2024-11-28 18-05-31](https://github.com/user-attachments/assets/b99a466b-a171-45ed-88ae-0926311e2acc)

- **Paths: Absolute & Relative**
  - Absolute path:Starts from the root (/) directory.

     cd /var
    
  - Relative path:Starts from the current working directory.

    cd /root/Desktop


### 7. Move Command
Move or rename files and directories:
- Rename

![Screenshot from 2024-11-28 18-27-49](https://github.com/user-attachments/assets/4dfcca43-6370-4619-a69c-dfc85a4dfb35)

- Move

![Screenshot from 2024-11-28 18-29-42](https://github.com/user-attachments/assets/0dae017f-f825-446a-bd45-815d6f71aa3c)


### 8. Copy Command
- Copy a folder with its contents:

![Screenshot from 2024-11-28 18-34-03](https://github.com/user-attachments/assets/1d717cd2-f9a3-4daa-93d8-bbd50e3fc295)

- Copy file content to another file:

![Screenshot from 2024-11-28 18-39-34](https://github.com/user-attachments/assets/8e749b4b-ce1d-4c9f-882c-0ab8c6c716ff)

### 9. TTY and Virtual Terminals
- Display terminal number:
   - tty
     - TTY stands for Teletypewriter, a term inherited from the early days of computing when physical terminals were used.
     - In modern Linux, a TTY represents a virtual terminal or text console that allows users to interact with the system.
     - Each TTY has a unique terminal number.

![Screenshot from 2024-11-28 18-43-16](https://github.com/user-attachments/assets/190d5613-75f8-4b6f-af0c-25a3cb105c30)


- Switch to a virtual terminal:
     - Virtual terminals are text-based user interfaces that run independently of the graphical desktop environment.
     - By default, Linux provides 6 virtual terminals  

![Screenshot from 2024-11-28 18-54-41](https://github.com/user-attachments/assets/27ace7ca-6a48-4c12-8804-d10fe37b4008)

![Screenshot from 2024-11-28 18-47-29](https://github.com/user-attachments/assets/c6fcb97b-754d-4860-a0e6-4f6c930b7559)


### 10. Getting Command Information

- date --help
- man ls
- pinfo mkdir
   - Navigation:
      - n: Next
      - p: Previous
      - d: Index

### 11. Editing with Vim
Basic Commands:
- Insert mode: Press i
- Save and exit: :wq!
- Set line numbers: :se nu
- Remove line numbers: :se nonu

Advanced Editing:
- Copy three line: 3yy, Paste: p
- Undo: u, Redo: Ctrl + r
- Delete 10 lines: 10d
- Copy 2 words: 2ya, Paste: p

![Screenshot from 2024-11-28 19-00-10](https://github.com/user-attachments/assets/2ee299b1-df1a-42bd-b1a6-2b575875cc91)
![Screenshot from 2024-11-28 19-00-24](https://github.com/user-attachments/assets/29664cc1-eb84-4da1-a7cc-e5c0adbf9b80)



