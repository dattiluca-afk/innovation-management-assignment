# How to start

## 1. Install Python

The setup instructions below use **Python 3.14**.

- **Windows:** Install the Python install manager from [python.org](https://www.python.org/downloads/) or the Microsoft Store, then open PowerShell and install Python 3.14:

  ```powershell
  py install 3.14
  ```

- **macOS:** Install Python 3.14 from [python.org](https://www.python.org/downloads/) or with Homebrew (`brew install python@3.14`).
- **Linux:** Install Python 3.14 and its `venv` support using your distribution's package manager. For example, on Ubuntu: `sudo apt install python3.14 python3.14-venv`.

Check that Python 3.14 is available:

```powershell
py -V:3.14 --version
```

On macOS or Linux, use:

```bash
python3.14 --version
```

## 2. Create and activate a virtual environment

Run these commands from the repository root.

**Windows (PowerShell):**

```powershell
py -V:3.14 -m venv .venv
.\.venv\Scripts\Activate.ps1
```

If you use Command Prompt instead of PowerShell, activate it with:

```bat
.venv\Scripts\activate.bat
```

**macOS or Linux:**

```bash
python3.14 -m venv .venv
source .venv/bin/activate
```

When the environment is active, install the packages listed in `requirements.txt`:

```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

`requirements.txt` is currently empty, so there are no project packages to install yet. Add project dependencies to that file as they are introduced, then rerun the install command.

To leave the virtual environment when you are finished:

```bash
deactivate
```
