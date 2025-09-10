# Python VENV Lab 🐍

A hands-on lab designed to teach you how to create, manage, and use **Python Virtual Environments (venv)**.  
This repository provides a simple, guided environment to practice isolating Python projects with their own dependencies.

---

## 📌 What is this?
Python projects often require specific library versions that may conflict with global installations.  
Virtual environments allow you to create **isolated Python environments** where each project can safely manage its own dependencies.

This lab is a **step-by-step learning resource** for:
- Creating Python virtual environments
- Activating & deactivating environments
- Installing project-specific dependencies
- Managing `requirements.txt`
- Practicing best practices for Python project structure  

---

## 🛠️ Prerequisites

- Python **3.6+** installed (check with `python3 --version` or `python --version`)
- Git (to clone this repository)
- A terminal or command prompt

---

## 🚀 Getting Started

1. **Clone this repository**
   ```bash
   git clone https://github.com/RedHatRanger/Python_VENV_Lab.git
   cd Python_VENV_Lab
   ```

2. **Create a virtual environment**
   ```bash
   python3 -m venv venv
   ```

3. **Activate the environment**
   - On Linux/Mac:
     ```bash
     source venv/bin/activate
     ```
   - On Windows (PowerShell):
     ```powershell
     venv\Scripts\Activate.ps1
     ```

4. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

5. **Deactivate when finished**
   ```bash
   deactivate
   ```

---

## 📂 Repository Structure
```
Python_VENV_Lab/
│── README.md          # Project documentation (this file)
│── requirements.txt   # Example requirements file
│── examples/          # Sample scripts to test venv usage
└── notes/             # Helpful notes and lab exercises
```

---

## 🎯 Learning Objectives
By the end of this lab you should be able to:
- Understand *why* we use `venv`
- Create and activate Python virtual environments
- Install packages locally to a project
- Freeze and share dependencies via `requirements.txt`
- Confidently manage project-specific Python environments

---

## 📘 Additional Resources
- [Python venv documentation](https://docs.python.org/3/library/venv.html)  
- [pip documentation](https://pip.pypa.io/en/stable/)  
- [Virtualenv vs venv](https://realpython.com/python-virtual-environments-a-primer/)  

---

## 🤝 Contributing
Found something that could be improved?  
Feel free to **fork and submit a pull request**! Contributions are welcome.

---

## 📜 License
This project is licensed under the **MIT License** – see the [LICENSE](LICENSE) file for details.
