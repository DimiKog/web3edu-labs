# Lab 01 — Wallets & Web3 Identity (Besu Edu‑Net)

🎓 Part of **Web3Edu Labs**  
🌐 Lab landing page: https://web3edu.dimikog.org/labs/wallets-keys  

---

## 🇬🇧 English

## Learning Objectives
By completing this lab, you will be able to:
- Explain how **wallets and addresses** form the basis of Web3 identity
- Understand the role of a **wallet** in a **permissioned blockchain**
- Describe how identity exists **before** transactions or smart contracts
- Recognize the **existence of cryptographic keys** without managing them directly

---

## Context & Concepts

**Identity in Web3 is cryptographic and network‑agnostic — but trust is defined by the network you join.**

In this lab, you explore how wallets, cryptographic keys, and addresses form the basis of identity in a permissioned Ethereum network based on **Hyperledger Besu**.

![Wallet, address, and network context](./diagrams/lab01-identity-network.png)

**The address stays the same. The network defines context and trust.**

Traditional systems rely on accounts and passwords.  
Web3 systems rely on:
- cryptographic key pairs
- locally controlled wallets
- network‑level trust

🔎 **Scope note**

In this lab, cryptographic keys (private/public) are treated at a **conceptual level only**.
You are **not expected to generate, export, or manage keys**.

A dedicated follow‑up lab will focus exclusively on:
- private vs public keys
- key generation and storage
- security implications and key loss

A wallet is:

> A local cryptographic tool that manages keys and signs messages for a specific blockchain network.

---

## Prerequisites
- Modern web browser (Chrome / Firefox / Brave)
- Browser wallet (MetaMask or equivalent)
- Besu Edu‑Net RPC details (provided by instructor)

### Environment
- **Network:** Besu Edu‑Net (permissioned QBFT)
- **Transactions:** Not required
- **Gas:** Not required

---

## Tools Used
This lab uses a set of standalone, read‑only Web3Edu lab tools:

- **Network Identifier** — Detects the active `chainId` and network context  
  https://dimikog.github.io/web3edu-lab-tools/tools/network-identifier/app/

- **Address Anatomy** — Visual inspection of Ethereum address structure  
  https://dimikog.github.io/web3edu-lab-tools/tools/address-anatomy/app/

- **Identity Scope Visualizer** — Same address, different network meaning  
  https://dimikog.github.io/web3edu-lab-tools/tools/identity-scope/app/

---

## Step-by-Step Instructions

### Step 1 — Configure your wallet for Besu Edu‑Net
Add Besu Edu‑Net as a custom network and switch to it.

### Step 2 — Create or select a wallet account
Ensure your wallet is connected and note your public address.

### Step 3 — Inspect your address
Observe format, length, and checksum casing.

### Step 4 — Understand the key relationship (conceptual)

At this stage, you only need to understand the **existence and role** of keys.

```
Private Key  →  Public Key  →  Address
```

- This derivation is **one‑way**
- The wallet manages keys **on your behalf**
- The address represents your identity **on a given network**

⚠️ You are **not expected** to access, export, or manipulate keys in this lab.

📌 Key generation, storage, and security practices are covered in a **separate dedicated lab**.

✅ Expected outcome:  
You can conceptually explain how wallets, keys, and addresses relate, without handling keys directly.

### Step 5 — Identity without accounts
You now have identity without usernames or passwords.

---

## Exercises
Complete the following:

1. Identify your public address on Besu Edu‑Net
2. Explain how the same address can exist on multiple networks
3. Describe what information defines identity at this stage

---

## Reflection Questions
- Why does Web3 identity not require accounts?
- What happens if a private key is leaked?
- Why do we use a permissioned Besu network in this lab?

---

## What’s Next
➡️ **Lab 02 — Message Signing & Ownership**  
🌐 https://web3edu.dimikog.org/labs/message-signing

---

## 🇬🇷 Ελληνικά

## Μαθησιακοί Στόχοι
Με την ολοκλήρωση του εργαστηρίου θα μπορείτε:
- Να εξηγείτε τον ρόλο **ιδιωτικού κλειδιού**, **δημόσιου κλειδιού** και **διεύθυνσης** στην ταυτότητα Web3
- Να κατανοείτε τι είναι το **πορτοφόλι** σε ένα **αδειοδοτημένο blockchain**
- Να εξηγείτε πώς η ταυτότητα υπάρχει **πριν** από συναλλαγές ή smart contracts

---

## Εννοιολογικό Υπόβαθρο

**Η ταυτότητα στο Web3 είναι κρυπτογραφική και ανεξάρτητη δικτύου — η εμπιστοσύνη όμως καθορίζεται από το δίκτυο στο οποίο συμμετέχετε.**

Σε αυτό το εργαστήριο εξετάζετε πώς πορτοφόλια, κρυπτογραφικά κλειδιά και διευθύνσεις αποτελούν τη βάση της ταυτότητας σε ένα αδειοδοτημένο Ethereum δίκτυο βασισμένο σε **Hyperledger Besu**.

![Wallet, address, and network context](./diagrams/lab01-identity-network.png)

**Η διεύθυνση παραμένει ίδια. Το δίκτυο καθορίζει το πλαίσιο και την εμπιστοσύνη.**

Παραδοσιακά συστήματα βασίζονται σε λογαριασμούς και κωδικούς.  
Τα Web3 συστήματα βασίζονται σε:
- ζεύγη κρυπτογραφικών κλειδιών
- τοπικά ελεγχόμενα πορτοφόλια
- εμπιστοσύνη που ορίζεται από το δίκτυο

Το πορτοφόλι είναι:

> Ένα τοπικό κρυπτογραφικό εργαλείο που διαχειρίζεται κλειδιά και υπογράφει μηνύματα για ένα συγκεκριμένο blockchain δίκτυο.

---

## Προαπαιτούμενα
- Σύγχρονος browser (Chrome / Firefox / Brave)
- Πορτοφόλι browser (π.χ. MetaMask)
- Στοιχεία RPC για το Besu Edu‑Net (από τον/την διδάσκοντα/ουσα)

### Περιβάλλον
- **Δίκτυο:** Besu Edu‑Net (permissioned QBFT)
- **Συναλλαγές:** Δεν απαιτούνται
- **Gas:** Δεν απαιτείται

---

## Εργαλεία που Χρησιμοποιούνται
Το εργαστήριο χρησιμοποιεί αυτόνομα, read‑only εργαλεία Web3Edu:

- **Network Identifier** — Εντοπίζει το ενεργό `chainId` και το πλαίσιο δικτύου  
  https://dimikog.github.io/web3edu-lab-tools/tools/network-identifier/app/index.gr.html

- **Address Anatomy** — Οπτική ανάλυση της δομής διεύθυνσης Ethereum  
  https://dimikog.github.io/web3edu-lab-tools/tools/address-anatomy/app/index.gr.html

- **Identity Scope Visualizer** — Ίδια διεύθυνση, διαφορετικό νόημα ανά δίκτυο  
  https://dimikog.github.io/web3edu-lab-tools/tools/identity-scope/app/index.gr.html

---

## Βήματα Εργαστηρίου

### Βήμα 1 — Ρύθμιση πορτοφολιού για Besu Edu‑Net
Προσθέστε το Besu Edu‑Net ως custom network και επιλέξτε το.

### Βήμα 2 — Δημιουργία ή επιλογή λογαριασμού
Βεβαιωθείτε ότι το πορτοφόλι είναι ενεργό και σημειώστε τη δημόσια διεύθυνση.

### Βήμα 3 — Παρατήρηση διεύθυνσης
Ελέγξτε μορφή, μήκος και checksum.

### Βήμα 4 — Κατανόηση σχέσης κλειδιών
Ιδιωτικό κλειδί → Δημόσιο κλειδί → Διεύθυνση (μονόδρομη παραγωγή).

### Βήμα 5 — Ταυτότητα χωρίς λογαριασμούς
Έχετε ταυτότητα χωρίς username ή password.

---

## Ασκήσεις
Ολοκληρώστε τα παρακάτω:

1. Εντοπίστε τη δημόσια διεύθυνσή σας στο Besu Edu‑Net
2. Εξηγήστε πώς η ίδια διεύθυνση μπορεί να υπάρχει σε πολλά δίκτυα
3. Περιγράψτε ποια πληροφορία ορίζει την ταυτότητα σε αυτό το στάδιο

---

## Ερωτήσεις Αναστοχασμού
- Γιατί η ταυτότητα στο Web3 δεν χρειάζεται λογαριασμούς;
- Τι συμβαίνει αν διαρρεύσει το ιδιωτικό κλειδί;
- Γιατί χρησιμοποιούμε permissioned Besu δίκτυο σε αυτό το lab;

---

## Επόμενο Lab
➡️ **Lab 02 — Message Signing & Ownership**  
🌐 https://web3edu.dimikog.org/labs/message-signing

---

© Web3Edu
