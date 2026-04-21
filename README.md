A virtual file system built in C++, inspired by Linux, showcasing inode structure and file descriptor handling.


# Linux-Inspired Virtual File System

A Linux-inspired Virtual File System implemented in C++ that simulates core file system operations such as file creation, deletion, reading, and writing using inode-based architecture.

This project demonstrates how file systems work internally by using data structures and system-level programming concepts.

---

## Project Overview

This project is a command-line based Linux-inspired Virtual File System that simulates how a real file system works.

It supports basic operations such as:
- File creation
- File reading and writing
- File deletion
- Viewing file information
- Command help system

  All data is stored in memory using dynamic memory allocation (RAM-based system).
---

## Objectives

- Understand Linux File System Architecture
- Implement inode-based file management
- Simulate file operations
- Learn system programming concepts
- Improves data structures knowledge

---

## Technologies Used

| Technology                   | Purpose                     |
|------------------------------|-----------------------------|
| C++                          | Core implementation         |
| Data Structures              | Inode and file management   |
| Dynamic Memory Allocation    | File storage handling       |
| GCC / G++ Compiler           | Compilation                 |
| Command Line Interface (CLI) | User interaction            |

---

System Architecture

The Linux-Inspired Virtual File System is structured into multiple layers that simulate how a real file system works internally.

User Commands (CLI)
        |
        v
+----------------------+
|   Command Handler    |
| (Shell + Parser)     |
+----------------------+
        |
        v
+----------------------+
|        UAREA         |
| (UFDT - File Table)  |
+----------------------+
        |
        v
+----------------------+
|      File Table      |
| (Read/Write Offset,  |
|  Mode, Inode Link)   |
+----------------------+
        |
        v
+----------------------+
|        Inode         |
| (Metadata of File)   |
+----------------------+
        |
        v
+----------------------+
|     Data Buffer      |
| (Actual File Data)   |
+----------------------+

---

## Supported Commands

| Command                          | Description                  |
|----------------------------------|------------------------------|
| creat <name> <permission>        | Create a new file            |
| write <fd>                       | Write data into a file       |
| read <fd> <size>                 | Read data from a file        |
| unlink <name>                    | Delete a file                |
| ls                               | List all files               |
| man <command>                    | Display command manual       |
| help                             | Show all commands            |
| clear                            | Clear the terminal           |
| exit                             | Exit the system              |
