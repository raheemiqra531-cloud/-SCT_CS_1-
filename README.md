# 🔐 SCT_CS_1 — Caesar Cipher

> **SkillCraft Technology | Cyber Security Internship — Task 01**

---

## 📌 Task Description

Create a program that can **encrypt and decrypt text** using the Caesar Cipher algorithm. Allow users to input a message and a shift value to perform encryption and decryption.

---

## 🧠 What is Caesar Cipher?

The Caesar Cipher is one of the oldest and simplest encryption techniques. Each letter in the plaintext is shifted a fixed number of positions down or up the alphabet.

```
Plain:    A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
Shift 3:  D E F G H I J K L M N O P Q R S T U V W X Y Z A B C
```

**Example:**
- `Hello World` + Shift `3` → `Khoor Zruog`
- `Khoor Zruog` + Shift `3` → `Hello World`

---

## 📁 File Structure

```
SCT_CS_1/
├── caesar_cipher_cli.py   # Command-Line Interface version
├── caesar_cipher_gui.py   # Graphical User Interface version
└── README.md              # Project documentation
```

---

## ⚙️ Requirements

- Python 3.x
- `tkinter` (built-in with Python — for GUI version)
- No external libraries required

---

## 🚀 How to Run

### CLI Version
```bash
python caesar_cipher_cli.py
```

### GUI Version
```bash
python caesar_cipher_gui.py
```

---

## 🖥️ Features

### GUI
| Feature | Description |
|---|---|
| Encrypt Button | Encrypts entered message |
| Decrypt Button | Decrypts entered message |
| Brute Force Button | Shows all 25 possible decryptions |
| Copy Output | Copies result to clipboard |
| Clear Button | Resets all fields |
| Shift Spinbox | Easy 1–25 shift selector |

---

## 📸 Usage Example

```
===============================================
       CAESAR CIPHER — SkillCraft Technology
         Cyber Security Internship | Task 01
===============================================

Options:
  [1] Encrypt a message
  [2] Decrypt a message
  [3] Brute-force all shifts
  [0] Exit

Choose an option: 1
Enter message to encrypt: Hello World
Enter shift value (1–25): 3

  Original  : Hello World
  Shift     : 3
  Encrypted : Khoor Zruog
```

---

## 🔍 How It Works

```python
def caesar_cipher(text, shift, mode='encrypt'):
    if mode == 'decrypt':
        shift = -shift
    for char in text:
        if char.isalpha():
            base = ord('A') if char.isupper() else ord('a')
            shifted = (ord(char) - base + shift) % 26 + base
            result.append(chr(shifted))
```

- Letters are shifted using modular arithmetic (`% 26`) to wrap around the alphabet
- Non-alphabetic characters (spaces, numbers, punctuation) are preserved as-is
- Case sensitivity is maintained (uppercase stays uppercase)

---

## 👩‍💻 Author

**Iqra Raheem**
Cyber Security Intern — SkillCraft Technology
Internship ID: SCT/MAY26/0435

