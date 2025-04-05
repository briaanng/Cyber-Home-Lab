# 🔐 Lab 02 – Password Strength Testing with John the Ripper

## 🧠 Objective
Simulate how attackers test password strength by cracking SHA-256 password hashes using John the Ripper and a custom wordlist.

---

## 🛠️ Tools Used
- Kali Linux (running on MacBook via UTM)
- John the Ripper
- Terminal

---

## ⚙️ Steps

### 1. Created Passwords
```bash
echo "hello123" > passwords.txt
echo "P@ssw0rd" >> passwords.txt
echo "12345678" >> passwords.txt
echo "MySecurePassword2024!" >> passwords.txt

# Convert passwords to SHA-256 hashes
while read pass; do echo -n "$pass" | sha256sum; done < passwords.txt > hashes.txt

# Clean the hashes (remove extra formatting)
cut -d ' ' -f1 hashes.txt > clean_hashes.txt

# Run John the Ripper with custom wordlist
john --format=raw-sha256 clean_hashes.txt --wordlist=wordlist.txt

# Show any cracked passwords
john --show clean_hashes.txt

### 🔹 Step 2: Hashed the passwords using SHA-256
Used a terminal loop to convert each password into a SHA-256 hash and saved it into a file:
```bash
while read pass; do echo -n "$pass" | sha256sum; done < passwords.txt > hashes.txt

🔹 Step 3: Cleaned the hashes for John the Ripper
cut -d ' ' -f1 hashes.txt > clean_hashes.txt

🔹 Step 4: Created a custom wordlist
nano wordlist.txt

🔹 Step 5: Cracked the password hashes using John the Ripper
john --format=raw-sha256 clean_hashes.txt --wordlist=wordlist.txt

---
