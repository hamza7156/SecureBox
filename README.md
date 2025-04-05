SecureBox - Secure File Storage Web Application
Overview
SecureBox is a web application designed for secure file storage and management. Built as a solo development project, it leverages robust encryption, authentication, and security measures to ensure user data remains protected. The application allows users to upload, encrypt, and store files with restricted file types, while providing a seamless experience across desktop and mobile platforms.

Features
Client-Side Encryption: Files are encrypted before upload using Fernet (AES-128-CBC with HMAC-SHA256).
Strong Password Enforcement: Users must create passwords with uppercase letters, lowercase letters, numbers, and special characters.
Unique Usernames: Prevents username repetition for secure and distinct user identification.
Two-Factor Authentication (2FA): Time-based One-Time Passwords (TOTP) via PyOTP, compatible with Google Authenticator.
Rate Limiting: Restricts login attempts to mitigate brute-force attacks.
CSRF Protection: Secures form submissions against cross-site request forgery.
File Type Restrictions: Limits uploads to safe extensions (.txt, .pdf, .docx) to prevent malicious files.
Hardware Used
Development Machine
Laptop: Asus Zenbook Duo
Processor: Intel(R) Core(TM) i7-10510U CPU @ 1.80GHz
Graphics: Intel(R) UHD Graphics and NVIDIA GeForce MX250
RAM: 16 GB
Storage: 476 GB INTEL SSDPEKNW512G8 SSD
OS: Microsoft Windows 11 Home 64-bit 10.0.26100
Purpose: Coding, testing, and local server hosting with fast build times and multitasking support.
Testing Device
Android Device: Samsung Galaxy S22 Ultra
Processor: Qualcomm Snapdragon 8 Gen 1, Octa-Core, up to 3.0 GHz
RAM: 12 GB
OS: Android 13
Purpose: APK testing for compatibility and responsiveness on mobile platforms.
Tech Stack
Backend: Flask (Python)
Database: SQLite with SQLAlchemy 2.0.23
Encryption: Fernet (Python Cryptography 41.0.7)
Password Hashing: Flask-Bcrypt 1.0.1 (SHA-512 with salting)
2FA: PyOTP 2.9.0
Rate Limiting: Flask-Limiter 3.5.0
Form Security: Flask-WTF 1.2.1 (CSRF protection)
Installation

Clone the Repository:
git clone https://github.com/yourusername/securebox.git
cd securebox

Set Up a Virtual Environment:
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

Install Dependencies:
pip install -r requirements.txt

Run the Application:
python app.py

Open your browser and navigate to http://localhost:5000.
Usage
Register with a unique username and a strong password.
Enable 2FA using a TOTP app like Google Authenticator.
Upload files (.txt, .pdf, .docx) to securely store them.
Access your encrypted files anytime via the web interface.
Security Details
Encryption: Files are encrypted client-side using a key derived from user input and username (not stored server-side).
Password Security: Enforces strong passwords and hashes them with salted SHA-512.
Database Security: SQLAlchemy sanitizes queries to prevent SQL injection.
Brute-Force Protection: Login attempts limited to 5 per minute.
File Safety: Only safe file extensions are permitted.
Contributing
Contributions are welcome! Please fork the repository, create a feature branch, and submit a pull request with your changes.

License
This project is licensed under the MIT License - see the  file for details.

Acknowledgments
Built with open-source tools and libraries.
Tested on real hardware for optimal performance.
