# Toxic ☣️

> **A High-Performance VirusTotal TUI Dashboard**

<img width="327" height="208" alt="toxic" src="https://github.com/user-attachments/assets/0b6835ad-04cb-4c62-9b5d-67c08070eaef" />


**Toxic** is a modern, visual Terminal User Interface (TUI) for VirusTotal, built with Python and [Textual](https://textual.textualize.io/). It provides a seamless, keyboard-centric way to scan files, URLs, and domains directly from your terminal with a polished "Toxic Red & Cool Grey" aesthetic.

---

## ⚠️ Development Status

**Current Status: Active Development (Beta)**

This project is currently in active development. While the core scanning features and UI (v2.1) are stable, you may encounter bugs or incomplete features.
- **UI Version:** 2.1 (Toxic Red)
- **Core Logic:** Implemented
- **Auth:** Functional (Keyring integration)

---

## Key Features

*   **Visual Dashboard:** A beautiful, responsive TUI with high-resolution image rendering (via `textual-image`) and a custom design system.
*   **VirusTotal Integration:**
    *   **File Mode:** Scan local files (by path) or check existing hashes.
    *   **URL Mode:** Scan and analyze URLs.
    *   **Search Mode:** Investigate IP addresses, domains, and file hashes.
*   **Secure Authentication:**
    *   Securely stores your VirusTotal API Key using the system's native keyring service.
    *   Settings menu for easy key management.
*   **Reactive UI:** Real-time updates and smooth transitions between scanning modes.

## Installation & Usage

### Prerequisites
- Python 3.8+
- A [VirusTotal API Key](https://www.virustotal.com/gui/user/apikey)

### Setup

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/yourusername/toxic.git
    cd toxic
    ```

2.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

3.  **Run the application:**
    ```bash
    ./run.sh
    # OR
    python src/main.py
    ```

## Controls

Toxic is designed for both keyboard and mouse interaction.

| Key / Action | Description |
| :--- | :--- |
| **`s`** | Open **Settings** (Enter API Key) |
| **`q`** | **Quit** the application |
| **`Enter`** | Submit scan / Confirm action |
| **Click** | All buttons and tabs are clickable |

### Workflow
1.  Launch Toxic.
2.  Press `s` to open Settings and paste your VirusTotal API Key.
3.  Select a mode: **FILE**, **URL**, or **SEARCH**.
4.  Enter your target (path, URL, or hash) and press `SCAN` (or Enter).
5.  View detailed results in the markdown-rendered report view.

## Architecture

Toxic follows a modular architecture separating UI, Core Logic, and Authentication.

*   **Frontend (`src/ui/`):**
    *   Built with **Textual**, leveraging its CSS-like styling (`.tcss`) and widget system.
    *   **`screens.py`**: Contains the main application logic, including `MainScreen`, `SettingsScreen`, and `ResultsScreen`.
    *   **`style.tcss`**: Defines the "Toxic" design system (colors, layout, animations).
*   **Core (`src/core/`):**
    *   **`vt_client.py`**: Wrapper around `vt-py` to handle asynchronous API requests and data formatting.
*   **Authentication (`src/auth/`):**
    *   **`manager.py`**: Handles secure storage and retrieval of API keys using the `keyring` library.

<p align="center">
&copy; CodeFXR. All rights reserved.
</p>
