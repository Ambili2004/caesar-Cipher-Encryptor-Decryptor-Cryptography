# caesar-Cipher-Encryptor-Decryptor-Cryptography
in this program i use python for creating simple caesar Cipher Encryptor/Decryptor Cryptography as project 2
OUTPUT
<img width="858" height="310" alt="Screenshot 2026-04-02 150246" src="https://github.com/user-attachments/assets/3695c0c1-8255-4ecd-88cc-98d65aa23d75" /> 




# 🔐 Caesar Cipher — Encryptor / Decryptor

A Python-based command-line cryptography tool that implements the classic **Caesar Cipher** algorithm. Supports encryption, decryption, and brute-force attack to decode unknown ciphertexts.

---

## 📌 Table of Contents

- [About the Project](#about-the-project)
- [How It Works](#how-it-works)
- [Features](#features)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Examples](#examples)
- [Project Structure](#project-structure)
- [Tech Stack](#tech-stack)
- [Author](#author)

---

## 📖 About the Project

The **Caesar Cipher** is one of the oldest and simplest encryption techniques in cryptography. It works by shifting each letter in the plaintext by a fixed number of positions in the alphabet.

For example, with a shift of **3**:
```
Plain  : A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
Cipher : D E F G H I J K L M N O P Q R S T U V W X Y Z A B C
```

> `Hello World` → `Khoor Zruog`

This project was built to demonstrate how classical cryptography works using Python, with a clean interactive command-line interface.

---

## ⚙️ How It Works

### Encryption Formula
```
encrypted = chr((ord(char) - base + shift) % 26 + base)
```
- `base` is `65` for uppercase (A–Z) and `97` for lowercase (a–z)
- `% 26` ensures wrap-around (e.g., `Z + 1 = A`)
- Non-alphabetic characters (spaces, numbers, symbols) are left unchanged

### Decryption Formula
Decryption is just encryption with a **negative shift**:
```
decrypted = encrypt(text, -shift)
```

### Brute Force
Tries all **25 possible shifts** and prints the results so you can visually identify the original message.

---

## ✨ Features

- ✅ **Encrypt** — Convert plaintext to ciphertext using a shift key
- ✅ **Decrypt** — Recover original text using the correct shift key
- ✅ **Brute Force** — Try all 25 shifts to crack an unknown cipher
- ✅ **Input Validation** — Handles wrong choices, letters-as-numbers, out-of-range shifts
- ✅ **Preserves** spaces, digits, and punctuation
- ✅ **Case-sensitive** — Uppercase and lowercase letters are shifted independently

---

## 🚀 Getting Started

### Prerequisites

- Python 3.x installed on your machine
- No external libraries required — uses only Python built-ins

### Installation


## 💻 Usage

When you run the script, you will see an interactive menu:

```
=== Caesar Cipher ===

1. Encrypt
2. Decrypt
3. Brute Force

Choose (1/2/3):
```

Enter `1`, `2`, or `3` to select your desired operation.

> ⚠️ Only enter numbers (`1`, `2`, or `3`) at the menu prompt — not words like `hello`.

---

## 📋 Examples

### Encrypt
```
Choose (1/2/3): 1
Enter text  : Hello World
Enter shift (1-25): 3

✅ Encrypted : Khoor Zruog
```

### Decrypt
```
Choose (1/2/3): 2
Enter text  : Khoor Zruog
Enter shift (1-25): 3

✅ Decrypted : Hello World
```

### Brute Force
```
Choose (1/2/3): 3
Enter ciphertext: Khoor Zruog

Brute Force — all possible shifts:

  Shift  1: Lmnps Asvph
  Shift  2: Liops Bruqi
  Shift  3: Hello World   ← readable!
  Shift  4: Gdkkn Vnqkc
  ...
```

---

## 📁 Project Structure

```
caesar-cipher-encryptor-decryptor/
│
├── caesar_cipher.py      # Main Python script
└── README.md             # Project documentation
```

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3.x | Core programming language |
| `ord()` / `chr()` | ASCII character conversion |
| Built-in I/O | Command-line interaction |

---

## 🔐 Cryptography Note

The Caesar Cipher is a **substitution cipher** and is **not secure** for real-world use. It can be cracked instantly using brute force (only 25 possible keys). It is used here purely for **educational and demonstrative purposes**.

For modern encryption, consider algorithms like **AES**, **RSA**, or **ChaCha20**.

---

## 👤 Author 
> Built with ❤️ using Python — for learning cryptography fundamentals.
