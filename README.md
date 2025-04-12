# 🔐 USB Encryption Tool

A portable, cross-PC USB encryption utility that **automatically encrypts/decrypts files** stored on your USB drive using a password prompt. Built with Python, PyInstaller, and packaged with a professional Windows installer using Inno Setup.

> 🛡️ Lock and unlock sensitive files seamlessly — just plug in your USB and go!

---

## 🚀 Features

- 🔒 **AES Encryption** with password protection
- 🔁 **Auto-lock on unplug, unlock on reinsert**
- 💡 **Graphical Password Dialog** (no command-line)
- ☁️ **Unlimited password attempts**
- 💼 **Portable** — runs directly from the USB
- 🧳 **Minimizes to tray** with quit option
- 🎨 **Custom icon support**
- 📦 **Windows installer** included

---

## 📁 How It Works

- On first run, you’re prompted to set a password.
- All files inside `secure_files/` will be encrypted.
- When plugged back in, it prompts for your password and decrypts everything upon success.

---

## 📦 Download

Clone this repo or [download the latest release](https://github.com/your-username/usb-encryption-tool/releases/latest).

Or compile it yourself:

```bash
git clone https://github.com/your-username/usb-encryption-tool.git
cd usb-encryption-tool
```

## 🧩 Dependencies

- Python 3.x
- [cryptography](https://pypi.org/project/cryptography/)
- [pystray](https://pypi.org/project/pystray/)
- [Pillow](https://pypi.org/project/Pillow/)

Install with:

```bash
pip install cryptography pystray pillow
```

---

## ⚙️ Build Instructions

### 🔹 1. Compile the Script to `.exe`

```bash
pyinstaller --onefile --noconsole --icon=usb_lock.ico usb_lock.py
```

### 🔹 2. Prepare USB Folder Structure

```
USB/
├── usb_lock_win.exe       ← compiled app
├── run_usb_lock.bat       ← auto launcher
├── secure_files/          ← encrypted file folder
├── usb_lock.ico           ← optional custom icon
```

### 🔹 3. Build Windows Installer (Optional)

Use [Inno Setup](https://jrsoftware.org/isinfo.php) and run `usb_lock_installer.iss`.

✅ It will generate a `.exe` installer that installs directly to your USB.

---

## 🖼️ Tray Icon

The app minimizes to the system tray on Windows. Right-click the icon to quit the app.

---

## 🔁 Auto-Detect USB

The installer looks for a USB drive containing a file named `usb_target_marker` to install files to that drive automatically.

---

## 📜 License

MIT License. Feel free to fork, customize, and distribute.

---

## 💬 Contributing

Pull requests and improvements are welcome!

1. Fork the repo
2. Create your feature branch: `git checkout -b cool-feature`
3. Commit changes
4. Push to the branch
5. Open a PR!

---

## 💡 Ideas for the Future

- Auto-run setup via USB (cross-platform)
- Hidden file system or vault mode
- OTP/2FA login integration
- Mac/Linux compatibility (basic support already possible)

---

## 🙏 Credits

- Encryption: [`cryptography`](https://cryptography.io/)
- GUI and Tray: `tkinter`, `pystray`, `Pillow`
- Installer: [Inno Setup](https://jrsoftware.org/)

---

🔗 Stay safe, and encrypt smart. 💾🔐
