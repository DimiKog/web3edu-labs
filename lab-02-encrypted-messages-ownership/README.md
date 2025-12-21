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

## ⚠️ Important MetaMask Limitation (Educational Note)

MetaMask can only provide encryption public keys for accounts that exist **inside your own wallet**.

This means:
- You cannot encrypt a message for an arbitrary external address
- The receiver address must correspond to another account you control in MetaMask
- To simulate a sender/receiver scenario, create multiple accounts in MetaMask and switch between them

This is a **wallet-level limitation by design**, not a limitation of cryptography or Web3 itself.

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
- Να κατανοείτε ότι **δεν απαιτούνται συναλλαγές στο blockchain** για κρυπτογράφηση και υπογραφές
- Να αναγνωρίζετε πραγματικές Web3 εφαρμογές για κρυπτογραφημένα και υπογεγραμμένα μηνύματα

---

## Πλαίσιο & Έννοιες

**Η ιδιωτικότητα και η ιδιοκτησία στο Web3 ξεκινούν πριν από το blockchain.**

Στο Web3, τα πορτοφόλια δεν χρησιμοποιούνται μόνο για την υπογραφή συναλλαγών.  
Αποτελούν **γενικής χρήσης κρυπτογραφικά εργαλεία**, τα οποία μπορούν να χρησιμοποιηθούν για:

- κρυπτογράφηση δεδομένων  
- απόδειξη πατρότητας / ιδιοκτησίας  
- επαλήθευση πρόθεσης (intent)  
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

### ✍️ Υπογραφή (Ownership & Integrity / Ιδιοκτησία & Ακεραιότητα)

Η υπογραφή διασφαλίζει ότι:
- μόνο ο κάτοχος ενός ιδιωτικού κλειδιού θα μπορούσε να δημιουργήσει τη συγκεκριμένη υπογραφή
- οποιοσδήποτε μπορεί να επαληθεύσει **ποιος υπέγραψε** ένα μήνυμα

Αυτό παρέχει **αυθεντικότητα και ακεραιότητα**.

📌 Οι δύο αυτοί μηχανισμοί είναι **ανεξάρτητοι**, αλλά συχνά χρησιμοποιούνται **συνδυαστικά**.

---

## 🧭 Τι Είναι — και Τι Δεν Είναι — Αυτό το Εργαστήριο

### ✅ Τι είναι
- Χρησιμοποιεί πραγματική κρυπτογραφία  
- Χρησιμοποιεί το ζεύγος κλειδιών του πορτοφολιού σας  
- Εκτελείται εξ ολοκλήρου στον browser  
- Δεν απαιτεί συναλλαγές  
- Δεν χρησιμοποιεί smart contracts  
- Δεν αλληλεπιδρά με blockchain  

### ❌ Τι δεν είναι
- Δεν είναι εφαρμογή messaging  
- Δεν βασίζεται σε gas  
- Δεν βασίζεται σε λογαριασμούς (accounts)  

---

## 🔧 Προαπαιτούμενα

- Σύγχρονος browser (Chrome / Firefox / Brave)  
- Πορτοφόλι browser (MetaMask ή αντίστοιχο)  
- Ρυθμισμένο Besu Edu-Net (όπως στο Εργαστήριο 01)  

⚠️ **Δεν απαιτείται ETH ή EDU-D**

---

## 🌐 Περιβάλλον

- **Δίκτυο:** Besu Edu-Net (permissioned QBFT)  
- **Συναλλαγές:** Δεν απαιτούνται  
- **Gas:** Δεν απαιτείται  
- **Χρήση blockchain:** Καμία (off-chain κρυπτογραφία)

## ⚠️ Σημαντικός Περιορισμός MetaMask (Εκπαιδευτική Σημείωση)

Το MetaMask μπορεί να παρέχει δημόσια κλειδιά κρυπτογράφησης **μόνο για λογαριασμούς που υπάρχουν μέσα στο δικό σας πορτοφόλι**.

Αυτό σημαίνει ότι:
- Δεν μπορείτε να κρυπτογραφήσετε μήνυμα για οποιαδήποτε εξωτερική διεύθυνση
- Η διεύθυνση παραλήπτη πρέπει να αντιστοιχεί σε άλλον λογαριασμό που ελέγχετε στο MetaMask
- Για προσομοίωση αποστολέα/παραλήπτη, δημιουργήστε πολλαπλούς λογαριασμούς στο MetaMask και εναλλάσσεστε μεταξύ τους

Αυτός είναι **περιορισμός του πορτοφολιού (wallet-level) από σχεδιασμό**, όχι περιορισμός της κρυπτογραφίας ή του Web3.

---

## Βήματα Εργαστηρίου

### Βήμα 1 — Κατανόηση μοντέλου κλειδιών (εννοιολογικά)

```
Ιδιωτικό Κλειδί  →  Δημόσιο Κλειδί  →  Διεύθυνση
```

- Το **ιδιωτικό κλειδί** δεν φεύγει ποτέ από το πορτοφόλι
- Το **δημόσιο κλειδί** μπορεί να κοινοποιηθεί
- Η **διεύθυνση** προκύπτει από το δημόσιο κλειδί

Σε αυτό το εργαστήριο, το πορτοφόλι:
- κρυπτογραφεί μηνύματα
- αποκρυπτογραφεί μηνύματα
- υπογράφει μηνύματα
- επαληθεύει υπογραφές

---

### Βήμα 2 — Κρυπτογράφηση μηνύματος (ιδιωτικότητα)

1. Επιλέξτε μια **δημόσια διεύθυνση παραλήπτη**
2. Γράψτε ένα σύντομο μήνυμα
3. Κρυπτογραφήστε το μήνυμα χρησιμοποιώντας το **δημόσιο κλειδί** του παραλήπτη

🔐 Αποτέλεσμα:
- Το κρυπτογραφημένο μήνυμα δεν είναι αναγνώσιμο
- Μόνο ο παραλήπτης μπορεί να το αποκρυπτογραφήσει

✅ Αναμενόμενο αποτέλεσμα:  
Κατανοείτε πώς η κρυπτογράφηση προστατεύει την εμπιστευτικότητα του μηνύματος.

---

### Βήμα 3 — Αποκρυπτογράφηση του μηνύματος (πλευρά παραλήπτη)

1. Χρησιμοποιήστε το πορτοφόλι του παραλήπτη
2. Αποκρυπτογραφήστε το κρυπτογραφημένο φορτίο (payload)

🔓 Αποτέλεσμα:
- Το αρχικό μήνυμα αποκαλύπτεται
- Δεν υπήρξε αλληλεπίδραση με το blockchain

✅ Αναμενόμενο αποτέλεσμα:  
Κατανοείτε ότι η κρυπτογράφηση/αποκρυπτογράφηση γίνεται **τοπικά**.

---

### Βήμα 4 — Υπογραφή κρυπτογραφημένου μηνύματος (ιδιοκτησία)

1. Πάρτε το κρυπτογραφημένο μήνυμα
2. Υπογράψτε το με το πορτοφόλι σας

✍️ Αυτό αποδεικνύει:
- ποιος έστειλε το μήνυμα
- ότι το μήνυμα δεν αλλοιώθηκε

✅ Αναμενόμενο αποτέλεσμα:  
Κατανοείτε πώς η υπογραφή εδραιώνει την ιδιοκτησία.

---

### Βήμα 5 — Επαλήθευση αποστολέα

1. Επαληθεύστε την υπογραφή
2. Ανακτήστε τη διεύθυνση αποστολέα
3. Συγκρίνετέ την με τον αναμενόμενο αποστολέα

✅ Αναμενόμενο αποτέλεσμα:  
Μπορείτε να επαληθεύσετε **ποιος έστειλε το μήνυμα**, χωρίς να εμπιστεύεστε έναν διακομιστή.

---

### Βήμα 6 — Συνδυασμός κρυπτογράφησης + υπογραφής

Έχετε:
- 🔐 Ιδιωτικότητα
- ✍️ Αυθεντικότητα

Αυτό είναι το θεμέλιο για:
- ασφαλή μηνύματα
- διακυβέρνηση DAO
- off-chain ψηφοφορίες
- ιδιωτικές βεβαιώσεις (attestations)
- κρυπτογραφημένα μεταδεδομένα SBT

---

## Ασκήσεις

1. Εξηγήστε τη διαφορά μεταξύ κρυπτογράφησης και υπογραφής.
2. Περιγράψτε γιατί η κρυπτογράφηση δεν απαιτεί blockchain.
3. Αναφέρετε πραγματικά παραδείγματα Web3 χρήσεων για κρυπτογραφημένα μηνύματα.

---

## Ερωτήσεις Αναστοχασμού

- Γιατί η ιδιωτικότητα είναι συχνά πιο σημαντική από τις συναλλαγές στο Web3;
- Τι συμβαίνει αν παραβιαστεί το ιδιωτικό κλειδί;
- Γιατί αυτές οι λειτουργίες υλοποιούνται εκτός blockchain και όχι on‑chain;

---

## Ολοκλήρωση Εργαστηρίου

🎯 Ολοκληρώσατε το **Εργαστήριο 02 — Κρυπτογραφημένα Μηνύματα & Ιδιοκτησία**.

Επιστρέψτε στο **Web3Edu** για να:
- σημειώσετε το εργαστήριο ως ολοκληρωμένο
- ενημερώσετε το μαθησιακό σας προφίλ
- ξεκλειδώσετε το επόμενο εργαστήριο

👉 https://web3edu.dimikog.org/#/labs/encrypted-messages

---

© Web3Edu
