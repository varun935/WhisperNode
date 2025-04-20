```markdown
# WhisperNode 🔐

WhisperNode is a lightweight, LAN-based dead drop file server built with Flask. Designed for offline, secure, and ephemeral file sharing, it enables stealthy file drops over a local network with features like upload expiration, file-type restrictions, and a simple web interface. Perfect for secure internal transfers without touching the cloud.

## ✨ Features

- 📁 Local-only file transfer (no internet required)
- ⏳ Upload expiry system to auto-delete files after a certain time
- 🧹 File-type filtering to block executables and unwanted formats
- 🔐 Optional passphrase-based encryption using AES (via PBKDF2 and PyCryptodome)
- 📦 Lightweight architecture with just two folders: `backend` and `frontend`
- 🕵️ Silent network presence, ideal for internal use and air-gapped systems

## 🗂️ Project Structure

```
WhisperNode/
├── backend/
│   ├── main.py         # Flask backend
│   ├── config.py       # Config settings
│   └── utils.py        # Encryption, validation, and helper functions
├── frontend/
│   ├── templates/
│   │   ├── index.html
│   │   ├── success.html
│   └── static/
│       └── style.css
└── README.md
```

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/WhisperNode.git
cd WhisperNode
```

### 2. (Optional but Recommended) Create a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install Requirements

```bash
pip install -r requirements.txt
```

### 4. Run the Server

```bash
cd backend
python main.py
```

Then open your browser and go to `http://<your-VM-or-local-IP>:5000`.

## 🔒 Encryption Details

WhisperNode uses **AES (Advanced Encryption Standard)** for secure file encryption when a user supplies a passphrase. The encryption key is derived using `PBKDF2` (Password-Based Key Derivation Function 2), with SHA-256 for strong resistance against brute-force attacks.

Encryption is optional: if no passphrase is given, the file is stored as-is. Encrypted files can only be decrypted with the correct passphrase through a matching decryption interface.

## 🧾 License

This project is licensed under the [MIT License](LICENSE).

---

Built by Varun Chaitenya Sharma
```

---
