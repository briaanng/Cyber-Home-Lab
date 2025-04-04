# 🔐 Lab 02 – Password Strength Testing with John the Ripper

## 🧠 Objective
Simulate how attackers test password strength by cracking SHA-256 password hashes using John the Ripper and a custom wordlist.

---

## 🛠️ Tools Used
- Kali Linux (on MacBook via UTM)
- John the Ripper
- Terminal

---

## ⚙️ Steps

1. **Created passwords:**
```bash
echo "hello123" > passwords.txt
echo "P@ssw0rd" >> passwords.txt
echo "12345678" >> passwords.txt
echo "MySecurePassword2024!" >> passwords.txt

while read pass; do echo -n "$pass" | sha256sum; done < passwords.txt > hashes.txt

---

## 📸 Screenshots

### ✅ Wordlist Created in Nano
This shows the wordlist used to attempt cracking the SHA-256 hashes.

![Wordlist Edit](screenshots/wordlist_edit.png)
