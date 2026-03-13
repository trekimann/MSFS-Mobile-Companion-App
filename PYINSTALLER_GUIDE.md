# MSFS MOBILE COMPANION APP PyInstaller Instructions

To compile an executable version of MSFS Mobile Companion App using PyInstaller:

## 1. Install dependencies

```bash
pip install -r requirements.txt pyinstaller
```

## 2. Build for Windows

```bash
pyinstaller -F --onefile --add-data "templates;templates" --add-data "static;static" --add-data "SimConnect;SimConnect" glass_server.py
```

## 3. Build for Linux (including Bazzite)

```bash
pyinstaller -F --onefile --add-data "templates:templates" --add-data "static:static" --add-data "SimConnect:SimConnect" glass_server.py
```

### Notes for Bazzite users

- Bazzite can run the app natively as a Linux binary.
- This project still depends on Microsoft Flight Simulator SimConnect components, so simulator connectivity depends on the target MSFS environment and SimConnect compatibility.
- The generated binary is under `dist/glass_server`.
