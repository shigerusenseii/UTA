# UTA
![Icon](https://iili.io/FR55Gcv.md.png)
## Ultra Secure Hybrid File Encryption Tool

![Encryption Icon](https://img.shields.io/badge/Encryption-AES256%20%2B%20RSA4096-blueviolet?style=for-the-badge&logo=keys)
![Security Level](https://img.shields.io/badge/Security-Multi--Layered-green?style=for-the-badge&logo=shield)
![Python Version](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python)
[![License](https://img.shields.io/badge/License-MIT-lightgrey.svg?style=for-the-badge)](LICENSE)

---

## 🌟 Overview

The **UTA File Encryptor** is a robust and user-friendly desktop application designed to protect your sensitive files with state-of-the-art encryption techniques. Built with Python and Tkinter, it offers a hybrid encryption approach combining the speed of AES-256 for data encryption with the unbreakability of RSA-4096 for secure key exchange.

Whether you need to secure a single document or an entire directory, UTA File Encryptor provides a reliable solution to keep your data confidential and safe from unauthorized access.

---

## ✨ Features

* **Hybrid Encryption:** Leverages a powerful combination of AES-256 for symmetric data encryption and RSA-4096 for asymmetric key encryption.
* **Two Encryption Methods:**
    * **Password-Based Encryption:** Encrypt files using a strong, user-defined password, deriving the AES key with PBKDF2 (100,000 iterations, SHA256) for enhanced security against brute-force attacks.
    * **RSA Key Pair Encryption:** Automatically generates a unique RSA-4096 key pair for each encryption operation. The public key encrypts a randomly generated AES key, while the private key (which you must securely store) is required for decryption.
* **Multi-Layered Security:** Incorporates random salts and Initialization Vectors (IVs) for each encryption, ensuring that identical plaintexts result in different ciphertexts.
* **File Integrity Check:** Uses SHA-256 checksums to verify file integrity during decryption, ensuring that the decrypted data has not been tampered with.
* **Intuitive GUI:** A clean and easy-to-use graphical interface built with Tkinter, making encryption and decryption accessible to everyone.
* **Cross-Platform (Python):** Being a Python application, it can run on various operating systems (Windows, macOS, Linux) where Python and its dependencies are installed.

---

## 🚀 Getting Started

### Prerequisites

Before you can run the UTA File Encryptor, you need to have Python 3.x installed on your system.
The application also relies on the `cryptography` library.

1.  **Install Python 3:**
    Download and install Python from [python.org](https://www.python.org/downloads/).

2.  **Install Dependencies:**
    Open your terminal or command prompt and run:
    ```bash
    pip install cryptography
    ```

### Installation

1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/shigerusenseii/UTA.git
    cd UTA
    ```

### Usage

1.  **Run the Application:**
    ```bash
    python uta.py
    ```

2.  **Encrypting a File:**
    * Click "ENCRYPT FILE".
    * Select the file you wish to encrypt.
    * Choose your desired encryption method:
        * **Encrypt with Password:** Enter and confirm a strong password (at least 8 characters). **Remember this password! It is essential for decryption.**
        * **Encrypt with RSA:** The application will generate an RSA key pair. A `.txt` file containing your private key will be saved alongside the encrypted file. **Store this private key file in an extremely secure location, as it is the only way to decrypt your file.**
    * An `.uta` extension will be added to your encrypted file.

3.  **Decrypting a File:**
    * Click "DECRYPT FILE".
    * Select the `.uta` encrypted file.
    * Provide the necessary key:
        * If encrypted with a password, enter the password you used.
        * If encrypted with RSA, you will be prompted to either load the private key from a file or paste it manually.
    * The decrypted file will be saved in the same directory, without the `.uta` extension.

---

## ⚠️ Important Security Notes

* **PASSWORD SECURITY:** If you encrypt with a password, **losing your password means your file will be permanently inaccessible.** There is no backdoor or recovery mechanism.
* **RSA PRIVATE KEY SECURITY:** If you encrypt with RSA, the generated private key is **crucial for decryption.** **If you lose this private key, your file cannot be decrypted.** Store it in a very secure and separate location from the encrypted file.
* **BACKUPS:** Always consider making a backup of your original files before encryption, especially when experimenting.

---

## 🤝 Contributing

Contributions are welcome! If you have suggestions for improvements, new features, or bug fixes, please feel free to open an issue or submit a pull request.

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 📞 Contact

For any inquiries or feedback, please reach out.
Email: oxxq@proton.me

---
