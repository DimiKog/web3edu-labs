# Lab 01 — Wallets, Keys & Web3 Identity (Besu Edu‑Net)

🎓 Part of **Web3Edu Labs**  
🌐 Lab landing page: https://web3edu.dimikog.org/labs/wallets-keys  

---

## 🇬🇧 English

## Learning Objectives
By completing this lab, you will be able to:
- Explain the role of **private keys**, **public keys**, and **addresses** in Web3 identity
- Understand what a **wallet** is in a **permissioned blockchain**
- Describe how identity exists **before** transactions or smart contracts

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

- **Network Identifier** — Detects the active `chainId` and network context *(web3edu‑lab‑tools)*
- **Address Anatomy** — Visual inspection of Ethereum address structure *(web3edu‑lab‑tools)*
- **Identity Scope Visualizer** — Same address, different network meaning *(web3edu‑lab‑tools)*

---

## Step-by-Step Instructions

### Step 1 — Configure your wallet for Besu Edu‑Net
Add Besu Edu‑Net as a custom network and switch to it.

### Step 2 — Create or select a wallet account
Ensure your wallet is connected and note your public address.

### Step 3 — Inspect your address
Observe format, length, and checksum casing.

### Step 4 — Understand the key relationship
Private key → Public key → Address (one‑way derivation).

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

- **Network Identifier** — Εντοπίζει το ενεργό `chainId` και το πλαίσιο δικτύου *(web3edu‑lab‑tools)*
- **Address Anatomy** — Οπτική ανάλυση της δομής διεύθυνσης Ethereum *(web3edu‑lab‑tools)*
- **Identity Scope Visualizer** — Ίδια διεύθυνση, διαφορετικό νόημα ανά δίκτυο *(web3edu‑lab‑tools)*

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
