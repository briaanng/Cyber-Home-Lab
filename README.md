# 🔐 Lab 02 – Password Strength Testing with John the Ripper

## 🧠 Objective
Understand how password cracking works by testing the strength of common passwords using hash values and a custom wordlist. This simulates what attackers do during a brute-force or dictionary attack.

---

## 🛠️ Tools Used
- 🐱‍💻 Kali Linux (UTM on Apple Silicon M4)
- 🧰 John the Ripper
- 📝 Custom wordlist and hash generator
- 💻 Terminal (CLI-focused)

---

## ⚙️ Setup & Steps

### 1️⃣ Created a file of sample passwords
```bash
echo "hello123" > passwords.txt
echo "P@ssw0rd" >> passwords.txt
echo "12345678" >> passwords.txt
echo "MySecurePassword2024!" >> passwords.txt
