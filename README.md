<div align="center">
  <img src="https://github.com/user-attachments/assets/0b6835ad-04cb-4c62-9b5d-67c08070eaef" alt="toxic_icon" width="220" />

  <h1>Toxic ☣️</h1>

  <p>
    <strong>A High-Performance VirusTotal TUI Dashboard built with Python.</strong>
  </p>

  <p>
    <img src="https://img.shields.io/badge/Made%20with-Textual-FF5F5F?style=flat-square" alt="Textual" />
    <img src="https://img.shields.io/badge/Language-Python-3776AB?style=flat-square&logo=python" alt="Python" />
    <img src="https://img.shields.io/badge/Status-Beta-orange?style=flat-square" alt="Status" />
    <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square" alt="License" />
  </p>

  <p>
    <a href="#"><strong>Documentation</strong></a> · 
    <a href="https://github.com/yourusername/toxic"><strong>Source Code</strong></a> · 
    <a href="https://github.com/yourusername/toxic/issues"><strong>Report Bug</strong></a>
  </p>
</div>

<br>

<p align="center">
  <img width="700" alt="toxic_main_demo" src="https://github.com/user-attachments/assets/0b6835ad-04cb-4c62-9b5d-67c08070eaef" />
</p>

<br>

## Why Toxic?

Toxic is a modern, visual Terminal User Interface (TUI) for VirusTotal. It provides a seamless, keyboard-centric way to scan threats with a polished "Toxic Red & Cool Grey" aesthetic.

- **Visual Dashboard:** A beautiful, responsive interface featuring high-resolution image rendering (via `textual-image`) and a custom design system.
- **VirusTotal Integration:** 
    - **File Mode:** Scan local files by path or check existing hashes.
    - **URL Mode:** Analyze suspicious URLs instantly.
    - **Search Mode:** Investigate IP addresses, domains, and hashes.
- **Secure Authentication:** Securely stores your API Key using the system's native keyring service—no plain-text keys in your history.
- **Reactive UI:** Built on an asynchronous engine for real-time updates and smooth transitions between scanning modes.
- **Local & Fast:** Designed for power users who need to investigate threats without leaving the command line.

## Installation

Get started by cloning the repository and installing the required Python dependencies.

```bash
# Clone the repository
git clone https://github.com/yourusername/toxic.git
cd toxic

# Install dependencies
pip install -r requirements.txt

# Run the application
./run.sh
# OR
python src/main.py
```

## Controls

Toxic is designed for both keyboard efficiency and mouse interaction.

| Context | Shortcut | Action |
| :--- | :--- | :--- |
| **Global** | `s` | Open **Settings** (API Key) |
| | `q` | **Quit** the application |
| **Navigation** | `Enter` | Submit scan / Confirm action |
| | `Tab` | Switch between input fields |
| **Interaction** | `Click` | All buttons and tabs are clickable |

## Architecture

Toxic follows a modular architecture separating the reactive frontend from the core API logic:

- **Frontend (`src/ui/`):** Leverages **Textual** and CSS-like styling (`.tcss`) for a reactive widget system.
- **Core Logic (`src/core/`):** An asynchronous wrapper around `vt-py` for efficient data formatting.
- **Authentication (`src/auth/`):** Handles secure storage via the `keyring` library to interface with system-level security.

<p align="center">
&copy; CodeFXR. All rights reserved.
</p>
```
