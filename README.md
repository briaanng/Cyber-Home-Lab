# 🔐 Lab 02 – Password Strength Testing with John the Ripper

## 🧠 Objective
Simulate how attackers test password strength by cracking SHA-256 password hashes using John the Ripper and a custom wordlist. This demonstrates how weak passwords are easily compromised and why secure password policies matter.

---

## 🛠️ Tools Used
- **Kali Linux** (running on MacBook Pro via UTM)
- **John the Ripper** (pre-installed on Kali)
- Terminal

---

## ⚙️ Steps

### 1. Created a list of sample passwords:
```bash
echo "hello123" > passwords.txt
echo "P@ssw0rd" >> passwords.txt
echo "12345678" >> passwords.txt
echo "MySecurePassword2024!" >> passwords.txt
