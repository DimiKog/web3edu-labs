# Lab 02 — Encrypted Messages & Ownership (Besu Edu‑Net)

🎓 Part of **Web3Edu Labs**  
🌐 Lab landing page: https://web3edu.dimikog.org/#/labs/encrypted-messages

---

## 🇬🇧 English

## Learning Objectives
By completing this lab, you will be able to:
- Explain the difference between **encryption** and **signing**
- Encrypt a message so that **only the intended receiver can read it**
- Sign a message to prove **ownership and authenticity**
- Understand that **encryption and signatures do not require blockchain transactions**
- Describe real Web3 use cases for encrypted and signed messages

---

## Context & Concepts

**Privacy and ownership in Web3 start before the blockchain.**

In Web3, wallets are not only used to sign transactions.  
They are general‑purpose cryptographic tools that can be used to:

- encrypt data
- prove authorship
- verify intent
- exchange messages securely

In this lab, you will explore **encrypted messaging** using wallet keys —  
**without smart contracts, without gas, and without sending transactions**.

---

## Key Concepts (Conceptual Overview)

### 🔐 Encryption (Confidentiality)
Encryption ensures that:
- anyone can encrypt a message using a **public key**
- only the owner of the corresponding **private key** can decrypt it

This provides **privacy**.

### ✍️ Signing (Ownership & Integrity)
Signing ensures that:
- only the owner of a private key could have created the signature
- anyone can verify who signed a message

This provides **authenticity and integrity**.

📌 These two mechanisms are **independent** but often used together.

---

## What This Lab Is — and Is Not

✅ Uses real cryptography  
✅ Uses your wallet’s key pair  
✅ Runs entirely in the browser  
✅ No transactions  
✅ No smart contracts  
✅ No blockchain interaction  

❌ Not a messaging app  
❌ Not gas‑based  
❌ Not account‑based  

---

## Prerequisites
- Modern web browser (Chrome / Firefox / Brave)
- Browser wallet (MetaMask or equivalent)
- Besu Edu‑Net configured (same as Lab 01)

⚠️ **No ETH or EDU‑D required**

---

## Environment
- **Network:** Besu Edu‑Net (permissioned QBFT)
- **Transactions:** Not required
- **Gas:** Not required
- **Blockchain usage:** None (off‑chain cryptography)

---

## Step‑by‑Step Instructions

### Step 1 — Understand the key model (conceptual)

Every wallet controls a key pair:

```
Private Key  →  Public Key  →  Address
```

- The **private key never leaves the wallet**
- The **public key** can be shared
- The **address** is derived from the public key

In this lab, the wallet:
- encrypts messages
- decrypts messages
- signs messages
- verifies signatures

---

### Step 2 — Encrypt a message (confidentiality)

1. Choose a **receiver’s public address**
2. Write a short message
3. Encrypt the message using the receiver’s **public key**

🔐 Result:
- The encrypted message is unreadable
- Only the receiver can decrypt it

✅ Expected outcome:  
You understand how encryption protects message confidentiality.

---

### Step 3 — Decrypt the message (receiver side)

1. Use the receiver’s wallet
2. Decrypt the encrypted payload

🔓 Result:
- The original message is revealed
- No blockchain interaction occurred

✅ Expected outcome:  
You understand that encryption/decryption happens **locally**.

---

### Step 4 — Sign the encrypted message (ownership)

1. Take the encrypted message
2. Sign it with your wallet

✍️ This proves:
- who sent the message
- that the message was not altered

✅ Expected outcome:  
You understand how signing establishes authorship.

---

### Step 5 — Verify the sender

1. Verify the signature
2. Recover the sender’s address
3. Compare it with the expected sender

✅ Expected outcome:  
You can verify **who sent the message**, without trusting a server.

---

### Step 6 — Combine encryption + signing

You now have:
- 🔐 **Confidentiality** (encryption)
- ✍️ **Authenticity** (signature)

This is the foundation of:
- secure messaging
- DAO governance
- off‑chain voting
- private attestations
- encrypted SBT metadata

---

## Exercises

1. Explain the difference between encryption and signing
2. Describe why encryption does not require a blockchain
3. Identify real Web3 use cases for encrypted messages

---

## Reflection Questions
- Why is encryption more important than transactions for privacy?
- What happens if a private key is compromised?
- Why is this done off‑chain instead of on‑chain?

---

## Lab Completion

🎯 You have completed **Lab 02 — Encrypted Messages & Ownership**.

Return to **Web3Edu** to:
- mark the lab as completed
- update your learning profile
- unlock the next lab

👉 https://web3edu.dimikog.org/#/labs/encrypted-messages

---

## 🇬🇷 Ελληνικά

## Μαθησιακοί Στόχοι
Με την ολοκλήρωση του εργαστηρίου θα μπορείτε:
- Να εξηγείτε τη διαφορά μεταξύ **κρυπτογράφησης** και **υπογραφής**
- Να κρυπτογραφείτε μηνύματα ώστε **μόνο ο παραλήπτης να μπορεί να τα διαβάσει**
- Να υπογράφετε μηνύματα για απόδειξη **ιδιοκτησίας και αυθεντικότητας**
- Να κατανοείτε ότι **δεν απαιτείται blockchain** για κρυπτογράφηση και υπογραφές
- Να αναγνωρίζετε πραγματικές Web3 εφαρμογές ασφαλούς επικοινωνίας

---

## Εννοιολογικό Υπόβαθρο

**Η ιδιωτικότητα και η ιδιοκτησία στο Web3 ξεκινούν εκτός blockchain.**

Τα πορτοφόλια Web3 δεν χρησιμοποιούνται μόνο για συναλλαγές.  
Αποτελούν γενικά κρυπτογραφικά εργαλεία για:

- κρυπτογράφηση δεδομένων
- απόδειξη ταυτότητας
- επαλήθευση προέλευσης
- ασφαλή ανταλλαγή μηνυμάτων

---

## Βήματα Εργαστηρίου

### Βήμα 1 — Κατανόηση κλειδιών (εννοιολογικά)

```
Ιδιωτικό Κλειδί  →  Δημόσιο Κλειδί  →  Διεύθυνση
```

Το πορτοφόλι:
- δεν αποκαλύπτει το ιδιωτικό κλειδί
- εκτελεί κρυπτογραφικές πράξεις για εσάς

---

### Βήμα 2 — Κρυπτογράφηση μηνύματος

- Επιλέξτε παραλήπτη
- Κρυπτογραφήστε το μήνυμα με το δημόσιο κλειδί του

🔐 Μόνο ο παραλήπτης μπορεί να το διαβάσει.

---

### Βήμα 3 — Αποκρυπτογράφηση

- Ο παραλήπτης αποκρυπτογραφεί το μήνυμα τοπικά

🔓 Χωρίς blockchain.

---

### Βήμα 4 — Υπογραφή μηνύματος

- Υπογράψτε το κρυπτογραφημένο μήνυμα

✍️ Απόδειξη ιδιοκτησίας.

---

### Βήμα 5 — Επαλήθευση αποστολέα

- Επαληθεύστε την υπογραφή
- Ανακτήστε τη διεύθυνση αποστολέα

---

### Βήμα 6 — Τι μάθατε

Έχετε:
- 🔐 Ιδιωτικότητα
- ✍️ Αυθεντικότητα

Αυτά αποτελούν τη βάση του Web3.

---

## Ολοκλήρωση Εργαστηρίου

🎯 Ολοκληρώσατε το **Lab 02 — Encrypted Messages & Ownership**.

👉 https://web3edu.dimikog.org/#/labs/encrypted-messages

---

© Web3Edu
