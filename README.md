A virtual file system built in C++, inspired by Linux, showcasing inode structure and file descriptor handling.


# Linux-Inspired Virtual File System

A Linux-inspired Virtual File System implemented in C++ that simulates core file system operations such as file creation, deletion, reading, and writing using inode-based architecture.

This project demonstrates how file systems work internally by using data structures and system-level programming concepts.

---

## 📌Project Overview

This project is a command-line based Linux-inspired Virtual File System that simulates how a real file system works.

It supports basic operations such as:
- File creation
- File reading and writing
- File deletion
- Listing file details (basic information)
- Command help system
All data is stored in memory using dynamic memory allocation (RAM-based system).
---

## 🎯 Objectives

- Understand Linux File System Architecture
- Implement inode-based file management
- Simulate file operations
- Learn system programming concepts
- Strengthen data structures knowledge

---

## ⚙️ Technologies Used

| Technology                   | Purpose                     |
|------------------------------|-----------------------------|
| C++                          | Core implementation         |
| Data Structures              | Inode and file management   |
| Dynamic Memory Allocation    | File storage handling       |
| GCC / G++ Compiler           | Compilation                 |
| Command Line Interface (CLI) | User interaction            |

---

## 🏗️ System Architecture

The Linux-Inspired Virtual File System is structured into multiple layers that simulate how a real file system works internally.

```
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
```

---

## 📜 Supported Commands

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

---

## ⚙️ How to Run

### 1. Clone the repository
git clone https://github.com/your-username/linux-inspired-vfs.git

### 2. Navigate to project folder
cd linux-inspired-vfs

### 3. Compile the code
g++ linux_inspired_vfs.cpp -o vfs

### 4. Run the program
./vfs

---

## 📸 Sample Execution

Linux-Inspired VFS : > creat file1 3  
File gets successfully created with FD 3  

Linux-Inspired VFS : > write 3  
Enter the data that you want to write :  
Hello World  

Linux-Inspired VFS : > read 3 5  
Data from file is : Hello  

Linux-Inspired VFS : > ls  
1    file1    11  

---

## ⚠️ Limitations 
- Data is stored only in RAM, so it is lost after program exits
- Limited number of files due to fixed inode count (MAXINODE)
- No directory structure (all files are in a single level)
- Only basic read/write permissions, no advanced access control

---

## 🔮 Future Enhancements
- Implement file persistence (store data permanently on disk)
- Add directory structure for better file organization (folders & hierarchy)
- Introduce open and close operations for realistic file handling
- Enhance permission system with execute access and better control

---

## 📚 Learning Outcomes
- Gained understanding of how a Linux-like file system works internally
- Learned implementation of inode-based file management
- Understood the concept of file descriptors and file tables
- Improved knowledge of data structures (linked list for inode management)

---

👨‍💻 Author
Tejas Pradip Sutar


