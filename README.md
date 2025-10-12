# Keylogger Assignment

## Description
This project is a keylogger script designed to run on Windows systems. It captures keystrokes, takes screenshots at random intervals, and sends the collected data via email. It also includes persistence mechanisms to start automatically on Windows login. This is intended for educational and controlled lab environments only.

## Requirements
- Python 3.0 or higher
- pynput
- pyautogui
- pywin32 (for Windows API access: win32gui, win32con, win32com.client)
- smtplib (standard Python library)
- email (standard Python library)
- Windows operating system (tested on Windows 10/11)
- Ensure you run this in an isolated lab environment for ethical and legal reasons

## Installation
To install the necessary Python packages, run the following command:

pip install pynput pyautogui pywin32


1. Configure the email credentials and SMTP settings in the script:

EMAIL_ADDRESS = 'your_email@example.com'
EMAIL_PASSWORD = 'your_email_password'
RECIPIENT_EMAIL = 'recipient_email@example.com'
SMTP_SERVER = 'smtp.example.com'
SMTP_PORT = 587

text

2. Run the script on a Windows machine with Python installed:

python keylogger.py (You Can Also Convert This .py File to .exe - through webistes).

## Important Notes

- This script is designed specifically for Windows and will not work on Linux or macOS without modifications.
- Running keyloggers may violate privacy laws and ethical guidelines. Use this script only in controlled environments where you have explicit permission.
- Antivirus software may detect this script as malicious due to its behavior.
- Always test in isolated virtual machines or lab setups.
- Make sure to secure and handle any collected data responsibly.

## Disclaimer
This project is for educational and research purposes only. The author is not responsible for any misuse or illegal activities conducted with this tool.

---

