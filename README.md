# 🐧 Linux OpenClassrooms - Learning Journey

![Linux](Linux.png)

> Personal repository documenting my Linux learning journey through OpenClassrooms. A comprehensive collection of notes, command references, exercises, and practical resources for mastering Linux fundamentals.

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Linux%20%7C%20Ubuntu-orange.svg)](https://ubuntu.com/)
[![Status](https://img.shields.io/badge/status-Active-success.svg)](https://github.com/Cristina-MariaG/linux_openClassrooms)

---

## 📚 Table of Contents

- [About](#-about)
- [Repository Structure](#-repository-structure)
- [Course Content](#-course-content)
- [Quick Start](#-quick-start)
- [Key Learning Topics](#-key-learning-topics)
- [Useful Resources](#-useful-resources)
- [Progress Tracker](#-progress-tracker)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🎯 About

This repository serves as my personal knowledge base while learning Linux through the **OpenClassrooms** platform. It contains structured notes, practical exercises, command references, and visual aids that helped me understand Linux from the ground up.

### Why This Repository?

- 📖 **Document Learning**: Track progress and key concepts
- 🔍 **Quick Reference**: Easy access to commands and solutions
- 💡 **Practical Examples**: Real-world use cases and exercises
- 🚀 **Knowledge Sharing**: Help others on their Linux journey
- 🔄 **Continuous Improvement**: Regular updates as I learn more

---

## 📂 Repository Structure

```
linux_openClassrooms/
│
├── 📄 README.md                        # This file
├── 🖼️  Linux.png                        # Main banner image
│
├── 📘 Course Notes
│   ├── chapitre1.md                    # Chapter 1: Linux Basics
│   └── chapitre2.md                    # Chapter 2: File System & Navigation
│
├── ⚡ Command References
│   └── commandes_linux_ubuntu.md       # Complete Ubuntu/Linux command cheat sheet
│
├── 📝 Exercises
│   └── exercices_chapitre2.md          # Practical exercises with solutions
│
├── 📊 Visual Resources
│   ├── image.png
│   ├── image-1.png
│   ├── image-2.png
│   ├── image-3.png
│   ├── image-4.png
│   └── image-5.png
│
└── 📄 References
    └── vi_cheat_sheet.pdf              # Vi/Vim editor quick reference
```

---

## 📖 Course Content

### Chapter 1: Introduction to Linux
**File**: [`chapitre1.md`](chapitre1.md)

- What is Linux and why use it?
- Linux distributions overview
- Command-line interface basics
- Terminal fundamentals
- User permissions and sudo

### Chapter 2: File System Navigation
**File**: [`chapitre2.md`](chapitre2.md)

- Linux file system hierarchy
- Navigating directories (`cd`, `pwd`, `ls`)
- File operations (create, move, copy, delete)
- File permissions and ownership
- Absolute vs relative paths

### Command Reference Guide
**File**: [`commandes_linux_ubuntu.md`](commandes_linux_ubuntu.md)

Complete reference of Linux commands organized by category:
- File management
- Directory operations
- System information
- Process management
- Network commands
- Text processing
- Package management (apt)

### Practical Exercises
**File**: [`exercices_chapitre2.md`](exercices_chapitre2.md)

Hands-on exercises covering:
- File system navigation challenges
- Permission management tasks
- Script creation
- Real-world scenarios

---

## 🚀 Quick Start

### Prerequisites

- Linux-based OS (Ubuntu recommended) or WSL on Windows
- Basic understanding of computer systems
- Terminal emulator access

### Getting Started

1. **Clone this repository**:
```bash
git clone https://github.com/Cristina-MariaG/linux_openClassrooms.git
cd linux_openClassrooms
```

2. **Explore the content**:
```bash
# View chapter notes
cat chapitre1.md

# Check command reference
less commandes_linux_ubuntu.md

# Try exercises
nano exercices_chapitre2.md
```

3. **Practice commands**:
```bash
# Use the command reference as a guide
# Practice in a safe test directory
mkdir ~/linux-practice
cd ~/linux-practice
```

---

## 🎓 Key Learning Topics

<table>
<tr>
<td width="50%">

### Core Concepts
- ✅ Terminal navigation
- ✅ File system structure
- ✅ User management
- ✅ Permissions (chmod, chown)
- ✅ Package management
- ✅ Process management

</td>
<td width="50%">

### Practical Skills
- ✅ Command-line efficiency
- ✅ Text editors (Vi/Vim, Nano)
- ✅ Shell scripting basics
- ✅ System monitoring
- ✅ Network tools
- ✅ Troubleshooting

</td>
</tr>
</table>

---

## 🔗 Useful Resources

### Official Documentation
- [Ubuntu Documentation](https://help.ubuntu.com/)
- [Linux Manual Pages](https://linux.die.net/man/)
- [GNU Coreutils](https://www.gnu.org/software/coreutils/manual/)

### Learning Platforms
- [OpenClassrooms - Linux Course](https://openclassrooms.com/)
- [Linux Journey](https://linuxjourney.com/)
- [The Linux Command Line Book](https://linuxcommand.org/tlcl.php)

### Quick References
- [Vi/Vim Cheat Sheet](vi_cheat_sheet.pdf) *(Included in this repo)*
- [Bash Cheat Sheet](https://devhints.io/bash)
- [Linux Command Library](https://linuxcommandlibrary.com/)

---

## 📊 Progress Tracker

| Chapter | Topic | Status | Date Completed |
|---------|-------|--------|----------------|
| 1 | Linux Basics | ✅ Complete | - |
| 2 | File System | ✅ Complete | - |
| 3 | Advanced Commands | 🔄 In Progress | - |
| 4 | Shell Scripting | 📅 Planned | - |
| 5 | System Administration | 📅 Planned | - |

---

## 💡 Tips for Learners

### Best Practices
```bash
# 1. Always use --help or man pages
man ls
ls --help

# 2. Practice in a test directory
mkdir ~/test && cd ~/test

# 3. Use tab completion
cd /usr/lo[TAB]  # Completes to /usr/local/

# 4. Check command history
history
!123  # Run command #123 from history

# 5. Use aliases for common commands
alias ll='ls -lah'
```

### Common Mistakes to Avoid
- ❌ Running `rm -rf /` without understanding
- ❌ Using `sudo` without verification
- ❌ Ignoring file permissions
- ❌ Not backing up important files
- ❌ Skipping `man` pages

---

## 🤝 Contributing

While this is primarily a personal learning repository, contributions are welcome!

### How to Contribute
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/improvement`)
3. Commit your changes (`git commit -m 'Add helpful tip'`)
4. Push to the branch (`git push origin feature/improvement`)
5. Open a Pull Request

### Contribution Ideas
- Fix typos or improve explanations
- Add more practical examples
- Suggest additional resources
- Share your own learning experiences

---

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

Feel free to use this content for your own learning journey!

---

## 🙏 Acknowledgments

- **OpenClassrooms** for the excellent Linux course
- The **Linux community** for extensive documentation
- **Ubuntu** for making Linux accessible
- Everyone who contributed to open-source documentation

---

## 📫 Contact

**Cristina-Maria G**

- GitHub: [@Cristina-MariaG](https://github.com/Cristina-MariaG)
- Repository: [linux_openClassrooms](https://github.com/Cristina-MariaG/linux_openClassrooms)

---

<div align="center">

### ⭐ If you find this helpful, please star the repository!

**Happy Learning! 🚀**

Made with ❤️ and lots of terminal commands

</div>
