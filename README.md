# WhisperNode 🔐

WhisperNode is a lightweight, LAN-based dead drop file server built with Flask. Designed for offline, secure, and ephemeral file sharing, it enables stealthy file drops over a local network with features like upload expiration, file-type restrictions, and a simple web interface. Perfect for secure internal transfers without touching the cloud.

## ✨ Features

- 📁 Local-only file transfer (no internet required)
- ⏳ Upload expiry system to auto-delete files after a certain time
- 🧹 File-type filtering to block executables and unwanted formats
- 🔐 Optional passphrase-based encryption using AES (via PBKDF2 and PyCryptodome)
- 📦 Lightweight architecture with just two folders: `backend` and `frontend`
- 🕵️ Silent network presence, ideal for internal use and air-gapped systems


## 🚀 Getting Started

### Clone the Repository

```bash
git clone https://github.com/varun935/WhisperNode.git
cd WhisperNode
```

### Create a Virtual Environment (Recommended)

```bash
python -m venv venv
```

```bash
source venv/bin/activate
```

*(Windows)*

```bash
venv\Scripts\activate
```

### Install Requirements

```bash
pip install -r requirements.txt
```

### Run the Server

```bash
cd backend
python main.py
```

## 🔒 Encryption Details

WhisperNode uses AES encryption through `PyCryptodome`, with keys derived using PBKDF2. Encryption is optional and passphrase-based — if the user provides a passphrase during upload, the file will be encrypted securely.

## 🧾 License

This project is licensed under the [MIT License](LICENSE).

---

Built by Varun Chaitenya Sharma
```
