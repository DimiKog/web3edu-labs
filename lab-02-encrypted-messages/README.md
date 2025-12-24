# Lab 02 — Encrypted Messages

🎓 Part of **Web3Edu Labs**  
🌐 Lab landing page: https://web3edu.dimikog.org/#/labs/encrypted-messages

---

## 🇬🇧 English

## Learning Objectives
By completing this lab, you will be able to:
- Encrypt a message so that **only the intended receiver can read it**
- Understand that **encryption does not require blockchain transactions**
- Describe real Web3 use cases for encrypted messages

---

## Context & Concepts

**Privacy and ownership in Web3 start before the blockchain.**

In Web3, wallets are not only used to send transactions.  
They are general‑purpose cryptographic tools that can be used to:

- encrypt data
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

---

## What This Lab Is — and Is Not

✅ Uses real cryptography  
✅ Uses your wallet’s key pair  
✅ Runs entirely in the browser  
✅ No transactions  
✅ No smart contracts  
✅ No blockchain interaction  
✅ No message delivery or storage  

❌ Not a messaging app  
❌ Not gas‑based  
❌ Not account‑based  

---

## Prerequisites
- Modern web browser (Chrome / Firefox / Brave)
- Besu Edu‑Net configured (same as Lab 01)

⚠️ **No ETH or EDU‑D required**

---

## Environment
- **Network:** Besu Edu‑Net (permissioned QBFT)
- **Transactions:** Not required
- **Gas:** Not required
- **Blockchain usage:** None (off‑chain cryptography)

## Step‑by‑Step Instructions

### Step 1 — Understand the key model (conceptual)

### Step 1a — Generate cryptographic identity (Key Generator tool)

👉 https://dimikog.github.io/web3edu-lab-tools/tools/key-generator/app/

### 🔁 End‑to‑End Cryptographic Flow (Lab 02)

```
┌────────────────────┐
│   Key Generator    │
│  (Educational)     │
│                    │
│  Input Text        │
│      ↓             │
│  Private Key       │
│      ↓             │
│  Public Key        │
│      ↓             │
│  Address           │
└─────────┬──────────┘
          │
          │  (share public key)
          ▼
┌────────────────────┐
│ Message Encryptor  │
│                    │
│  Message +         │
│  Receiver Public   │
│  Key               │
│      ↓             │
│  Encrypted Payload │
└─────────┬──────────┘
          │
          │  (send encrypted data)
          ▼
┌────────────────────┐
│ Message Decryptor  │
│                    │
│  Encrypted Payload │
│  + Private Key     │
│      ↓             │
│  Original Message  │
└────────────────────┘
```

📌 **Key takeaway:**  
Public keys enable **encryption**.  
Private keys enable **decryption**.  
Ownership equals control of the private key.

Before using wallets for encryption, you will first generate a cryptographic identity manually.

Using the **Key Generator** tool, you will:
- provide a text input (educational only)
- hash the input with **keccak256** (Ethereum-style)
- interpret the hash as a 256‑bit **private key** (secp256k1)
- derive the corresponding **public key**
- derive an Ethereum‑style **address**

This tool helps you understand where keys and addresses come from,
without relying on wallet software or hidden randomness.

📌 You will use the **public key** generated here in the Message Encryptor tool.
Encryption requires a public key, not an address.

Outputs are shown as a JSON object:
```json
{
  "input": "alice",
  "privateKey": "0x…",
  "publicKey": "0x…",
  "address": "0x…"
}
```

⚠️ This process is **deterministic**:
- the same input always produces the same keys
- this is intentional for learning purposes (not how real wallets generate keys)

This tool is **not a wallet** and does **not** store keys securely.  
Never use these keys for real funds.

Every wallet controls a key pair:

```
Private Key  →  Public Key  →  Address
```

- The **private key never leaves the wallet**
- The **public key** can be shared
- The **address** is derived from the public key

In this lab, the tools:
- encrypt messages
- decrypt messages

---

### Step 2 — Encrypt a message (Confidentiality)

👉 https://dimikog.github.io/web3edu-lab-tools/tools/message-encryptor/app/

1. Choose the receiver’s public key (from the Key Generator tool)
2. Write a short message
3. Encrypt the message using the receiver’s **public key**

🔐 Result:
- The encrypted message is unreadable
- Only the receiver can decrypt it

The encrypted output is a JSON payload containing:
- `version`
- `nonce`
- `ephemPublicKey`
- `ciphertext`

➡️ You must share the **full JSON payload** with the receiver.

✅ Expected outcome:  
You understand how encryption protects message confidentiality.

---

### Step 3 — Decrypt the message (receiver side)

👉 https://dimikog.github.io/web3edu-lab-tools/tools/message-decryptor/app/

1. Use the receiver’s private key (from the Key Generator)
2. Paste the encrypted JSON payload
3. Decrypt locally in the browser

🔓 Result:
- The original message is revealed
- No blockchain interaction occurred

✅ Expected outcome:  
You understand that encryption/decryption happens **locally**.

---

## Exercises

1. Describe why encryption does not require a blockchain
2. Identify real Web3 use cases for encrypted messages

---

## Reflection Questions
- Why is encryption more important than transactions for privacy?
- What happens if a private key is compromised?
- Why is this done off‑chain instead of on‑chain?

---

## Lab Completion

🎯 You have completed **Lab 02 — Encrypted Messages**.

Return to **Web3Edu** to:
- mark the lab as completed
- update your learning profile
- unlock the next lab

👉 https://web3edu.dimikog.org/#/labs/encrypted-messages

---

🔜 Next up: **signatures and ownership**.

## 🇬🇷 Ελληνικά

## Μαθησιακοί Στόχοι
Με την ολοκλήρωση του εργαστηρίου θα μπορείτε:
- Να κρυπτογραφείτε μηνύματα ώστε **μόνο ο παραλήπτης να μπορεί να τα διαβάσει**
- Να κατανοείτε ότι **δεν απαιτούνται συναλλαγές στο blockchain** για την κρυπτογράφηση
- Να αναγνωρίζετε πραγματικές Web3 εφαρμογές για κρυπτογραφημένα μηνύματα

---

## Πλαίσιο & Έννοιες

**Η ιδιωτικότητα και η ιδιοκτησία στο Web3 ξεκινούν πριν από το blockchain.**

Στο Web3, τα πορτοφόλια δεν χρησιμοποιούνται μόνο για την αποστολή συναλλαγών.  
Αποτελούν **γενικής χρήσης κρυπτογραφικά εργαλεία**, τα οποία μπορούν να χρησιμοποιηθούν για:

- κρυπτογράφηση δεδομένων  
- ασφαλή ανταλλαγή μηνυμάτων  

Σε αυτό το εργαστήριο, θα εξερευνήσετε την **κρυπτογραφημένη ανταλλαγή μηνυμάτων** χρησιμοποιώντας τα κλειδιά του πορτοφολιού σας —  
**χωρίς smart contracts, χωρίς gas και χωρίς συναλλαγές στο blockchain**.

---

## 🔑 Βασικές Έννοιες (Εννοιολογική Επισκόπηση)

### 🔐 Κρυπτογράφηση (Confidentiality / Ιδιωτικότητα)

Η κρυπτογράφηση διασφαλίζει ότι:
- οποιοσδήποτε μπορεί να κρυπτογραφήσει ένα μήνυμα χρησιμοποιώντας ένα **δημόσιο κλειδί**
- μόνο ο κάτοχος του αντίστοιχου **ιδιωτικού κλειδιού** μπορεί να το αποκρυπτογραφήσει

Αυτό παρέχει **ιδιωτικότητα**.

---

## 🧭 Τι Είναι — και Τι Δεν Είναι — Αυτό το Εργαστήριο

### ✅ Τι είναι
- Χρησιμοποιεί πραγματική κρυπτογραφία  
- Χρησιμοποιεί το ζεύγος κλειδιών του πορτοφολιού σας  
- Εκτελείται εξ ολοκλήρου στον browser  
- Δεν απαιτεί συναλλαγές  
- Δεν χρησιμοποιεί smart contracts  
- Δεν αλληλεπιδρά με blockchain  
- Δεν αποστέλλει ή αποθηκεύει μηνύματα  

### ❌ Τι δεν είναι
- Δεν είναι εφαρμογή messaging  
- Δεν βασίζεται σε gas  
- Δεν βασίζεται σε λογαριασμούς (accounts)  

---

## 🔧 Προαπαιτούμενα

- Σύγχρονος browser (Chrome / Firefox / Brave)  
- Ρυθμισμένο Besu Edu-Net (όπως στο Εργαστήριο 01)  

⚠️ **Δεν απαιτείται ETH ή EDU-D**

---

## 🌐 Περιβάλλον

- **Δίκτυο:** Besu Edu-Net (permissioned QBFT)  
- **Συναλλαγές:** Δεν απαιτούνται  
- **Gas:** Δεν απαιτείται  
- **Χρήση blockchain:** Καμία (off-chain κρυπτογραφία)

## Βήματα Εργαστηρίου

### Βήμα 1 — Κατανόηση μοντέλου κλειδιών (εννοιολογικά)

### Βήμα 1α — Δημιουργία κρυπτογραφικής ταυτότητας (εργαλείο Key Generator)

👉 https://dimikog.github.io/web3edu-lab-tools/tools/key-generator/app/index.gr.html

### 🔁 Ροή Κρυπτογραφίας από Άκρη σε Άκρη (Lab 02)

```
┌────────────────────┐
│   Key Generator    │
│  (Εκπαιδευτικό)    │
│                    │
│  Κείμενο Εισόδου   │
│      ↓             │
│  Ιδιωτικό Κλειδί   │
│      ↓             │
│  Δημόσιο Κλειδί    │
│      ↓             │
│  Διεύθυνση         │
└─────────┬──────────┘
          │
          │  (μοιράσου δημόσιο κλειδί)
          ▼
┌────────────────────┐
│ Message Encryptor  │
│                    │
│  Μήνυμα +          │
│  Δημόσιο Κλειδί    │
│  Παραλήπτη         │
│      ↓             │
│  Κρυπτογραφημένο   │
│  Payload           │
└─────────┬──────────┘
          │
          │  (στείλε κρυπτογραφημένα δεδομένα)
          ▼
┌────────────────────┐
│ Message Decryptor  │
│                    │
│  Κρυπτογραφημένο   │
│  Payload +         │
│  Ιδιωτικό Κλειδί   │
│      ↓             │
│  Αρχικό Μήνυμα     │
└────────────────────┘
```

📌 **Βασικό συμπέρασμα:**  
Τα δημόσια κλειδιά επιτρέπουν **κρυπτογράφηση**.  
Τα ιδιωτικά κλειδιά επιτρέπουν **αποκρυπτογράφηση**.  
Η ιδιοκτησία ισούται με τον έλεγχο του ιδιωτικού κλειδιού.

Πριν χρησιμοποιήσετε wallets για κρυπτογράφηση, θα δημιουργήσετε πρώτα
μια κρυπτογραφική ταυτότητα χειροκίνητα.

Χρησιμοποιώντας το εργαλείο **Key Generator**, θα:
- δώσετε ένα κείμενο εισόδου (μόνο για εκπαιδευτικούς σκοπούς)
- κάνετε hash της εισόδου με **keccak256** (τύπου Ethereum)
- ερμηνεύσετε το hash ως **ιδιωτικό κλειδί** 256‑bit (secp256k1)
- παράγετε το αντίστοιχο **δημόσιο κλειδί**
- παράγετε μια **διεύθυνση τύπου Ethereum**

Το εργαλείο αυτό σας βοηθά να κατανοήσετε από πού προέρχονται
τα κλειδιά και οι διευθύνσεις, χωρίς να βασίζεστε σε wallet
ή «κρυφή» τυχαιότητα.

📌 Θα χρησιμοποιήσετε το **δημόσιο κλειδί** που παράγεται εδώ
στο εργαλείο **Message Encryptor**.
Η κρυπτογράφηση απαιτεί δημόσιο κλειδί, όχι διεύθυνση.

Τα αποτελέσματα εμφανίζονται ως JSON:
```json
{
  "input": "alice",
  "privateKey": "0x…",
  "publicKey": "0x…",
  "address": "0x…"
}
```

⚠️ Αυτή η διαδικασία είναι **ντετερμινιστική**:
- η ίδια είσοδος παράγει πάντα τα ίδια κλειδιά
- αυτό είναι σκόπιμο για εκπαιδευτικούς λόγους (όχι όπως στα πραγματικά wallets)

Το εργαλείο **δεν είναι wallet** και **δεν** αποθηκεύει κλειδιά με ασφάλεια.  
Μην χρησιμοποιείτε αυτά τα κλειδιά για πραγματικά κεφάλαια.

```
Ιδιωτικό Κλειδί  →  Δημόσιο Κλειδί  →  Διεύθυνση
```

- Το **ιδιωτικό κλειδί** δεν φεύγει ποτέ από το πορτοφόλι
- Το **δημόσιο κλειδί** μπορεί να κοινοποιηθεί
- Η **διεύθυνση** προκύπτει από το δημόσιο κλειδί

Σε αυτό το εργαστήριο, τα εργαλεία:
- κρυπτογραφούν μηνύματα
- αποκρυπτογραφούν μηνύματα

---

### Βήμα 2 — Κρυπτογράφηση μηνύματος (Ιδιωτικότητα)

👉 https://dimikog.github.io/web3edu-lab-tools/tools/message-encryptor/app/index.gr.html

1. Επιλέξτε το **δημόσιο κλειδί του παραλήπτη** (από το εργαλείο Key Generator)
2. Γράψτε ένα σύντομο μήνυμα
3. Κρυπτογραφήστε το μήνυμα χρησιμοποιώντας το **δημόσιο κλειδί** του παραλήπτη

🔐 Αποτέλεσμα:
- Το κρυπτογραφημένο μήνυμα δεν είναι αναγνώσιμο
- Μόνο ο παραλήπτης μπορεί να το αποκρυπτογραφήσει

Το κρυπτογραφημένο αποτέλεσμα είναι JSON payload με:
- `version`
- `nonce`
- `ephemPublicKey`
- `ciphertext`

➡️ Πρέπει να μοιραστείτε **ολόκληρο** το JSON payload με τον παραλήπτη.

✅ Αναμενόμενο αποτέλεσμα:  
Κατανοείτε πώς η κρυπτογράφηση προστατεύει την εμπιστευτικότητα του μηνύματος.

---

### Βήμα 3 — Αποκρυπτογράφηση του μηνύματος (πλευρά παραλήπτη)

👉 https://dimikog.github.io/web3edu-lab-tools/tools/message-decryptor/app/index.gr.html

1. Χρησιμοποιήστε το ιδιωτικό κλειδί του παραλήπτη (από το Key Generator)
2. Επικολλήστε το κρυπτογραφημένο JSON payload
3. Αποκρυπτογραφήστε τοπικά στον browser

🔓 Αποτέλεσμα:
- Το αρχικό μήνυμα αποκαλύπτεται
- Δεν υπήρξε αλληλεπίδραση με το blockchain

✅ Αναμενόμενο αποτέλεσμα:  
Κατανοείτε ότι η κρυπτογράφηση/αποκρυπτογράφηση γίνεται **τοπικά**.

---

## Ασκήσεις

1. Περιγράψτε γιατί η κρυπτογράφηση δεν απαιτεί blockchain.
2. Αναφέρετε πραγματικά παραδείγματα Web3 χρήσεων για κρυπτογραφημένα μηνύματα.

---

## Ερωτήσεις Αναστοχασμού

- Γιατί η ιδιωτικότητα είναι συχνά πιο σημαντική από τις συναλλαγές στο Web3;
- Τι συμβαίνει αν παραβιαστεί το ιδιωτικό κλειδί;
- Γιατί αυτές οι λειτουργίες υλοποιούνται εκτός blockchain και όχι on‑chain;

---

## Ολοκλήρωση Εργαστηρίου

🎯 Ολοκληρώσατε το **Εργαστήριο 02 — Κρυπτογραφημένα Μηνύματα**.

Επιστρέψτε στο **Web3Edu** για να:
- σημειώσετε το εργαστήριο ως ολοκληρωμένο
- ενημερώσετε το μαθησιακό σας προφίλ
- ξεκλειδώσετε το επόμενο εργαστήριο

👉 https://web3edu.dimikog.org/#/labs/encrypted-messages

---

🔜 Επόμενο: **υπογραφές και ιδιοκτησία**.

© Web3Edu
