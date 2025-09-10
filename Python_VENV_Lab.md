# Python Virtual Environment Lab  

## Overview
This lab demonstrates how to set up and configure a Python virtual environment using `venv`, including alias creation, environment activation, and package management.

## Prerequisites
- Python 3.12 installed on your system  
- Basic command line knowledge  

---

## Lab Steps (Detailed)

### Step 1: Create Useful Aliases
```bash
alias pip3='python3.12 -m pip'
alias venv='python3.12 -m venv'
```
**Explanation**: Ensures you're using Python 3.12 explicitly for both pip and venv.

### Step 2: Create Virtual Environment
```bash
python3 -m venv .venv
```
**Explanation**: Creates a `.venv` directory with the environment.

### Step 3: Navigate to Environment Directory
```bash
cd .venv
```
**Explanation**: Move into the virtual environment directory to access config files.

### Step 4: Activate the Virtual Environment
```bash
source ./bin/activate
```
**Explanation**: Activates isolated environment, modifying `PATH`.

### Step 5: Modify Environment Configuration
```bash
sed -i 's/false/true/g' pyenv.cfg
```
**Explanation**: Changes `include-system-site-packages=false` → `true` for system-wide package access.

### Step 6: Verify Activation
```bash
echo $VIRTUAL_ENV
```
**Explanation**: Confirms the env path is active.

### Step 7: Install Dependencies
```bash
pip3 install -r requirements3.12.txt
```
**Explanation**: Installs packages from a requirements file.

### Step 8: Generate Requirements File
```bash
pip3 freeze > requirements.txt
```
**Explanation**: Captures all current installed versions.

### Step 9: Deactivate When Done
```bash
deactivate
```
**Explanation**: Exits back to system Python environment.

---

## Real-World Applications

### Web Development
```bash
python3 -m venv django_blog_env
source django_blog_env/bin/activate
pip install django==4.2.0 pillow psycopg2-binary
deactivate
```

### Data Science & Machine Learning
```bash
python3 -m venv ml_project_env
source ml_project_env/bin/activate
pip install tensorflow==2.13.0 pandas numpy jupyter
deactivate
```

### API Development
```bash
python3 -m venv api_service_env
source api_service_env/bin/activate
pip install fastapi uvicorn sqlalchemy
deactivate
```

### Legacy Apps
```bash
python2.7 -m virtualenv legacy_app_env
source legacy_app_env/bin/activate
pip install flask==1.1.4 requests==2.25.1
deactivate
```

### Client Project Isolation
```bash
# Client A
python3 -m venv client_a_env
source client_a_env/bin/activate
pip install django==3.2.0

# Client B
python3 -m venv client_b_env  
source client_b_env/bin/activate
pip install django==4.1.0
```

### Testing Package Versions
```bash
# Latest
python3 -m venv test_latest_env
source test_latest_env/bin/activate
pip install --upgrade requests flask

# Stable
python3 -m venv test_stable_env
source test_stable_env/bin/activate
pip install requests==2.28.0 flask==2.2.0
```

---

## Key Concepts Learned
- Virtual environment isolation  
- Simplifying commands with aliases  
- Editing `pyenv.cfg` for package access  
- Dependency management via `requirements.txt`  
- Environment life cycle: **activate → work → freeze → deactivate**  

---

## Best Practices
1. Always activate before installing packages  
2. Use descriptive names for environments  
3. Update and version-control `requirements.txt`  
4. Deactivate when switching environments  
5. Keep one environment per project  
6. Document setup steps in project notes or README  

---

## Troubleshooting
- If activation fails: check directory placement  
- If packages missing: confirm env with `echo $VIRTUAL_ENV`  
- If pip install fails: check Python version  
- Use `which python` to confirm you're inside `.venv`  
- To reset: close and reopen shell  

---

# Quick Reference Cheat Sheet (Short Version)

### Setup
```bash
alias pip3='python3.12 -m pip'
alias venv='python3.12 -m venv'
```

### Create Environment
```bash
python3 -m venv .venv
```

### Activate
```bash
source .venv/bin/activate
```

### Allow system packages (optional)
```bash
sed -i 's/false/true/g' .venv/pyenv.cfg
```

### Verify
```bash
echo $VIRTUAL_ENV
```

### Install
```bash
pip3 install -r requirements3.12.txt
```

### Save
```bash
pip3 freeze > requirements.txt
```

### Deactivate
```bash
deactivate
```

**Flow summary**:  
```bash
python3 -m venv .venv && source .venv/bin/activate && pip install -r requirements.txt && deactivate
```
