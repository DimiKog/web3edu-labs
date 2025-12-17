# 🧪 Lab 01 — Wallets, Keys & Web3 Identity (Besu Edu-Net)

---

## 🇬🇧 English

## Table of Contents

- [Core concept](#core-concept)
- [Learning objectives](#-learning-objectives)
- [Prerequisites](#-prerequisites)
- [Conceptual background](#-conceptual-background-read-carefully)
- [Environment](#-environment)
- [Lab steps](#-lab-steps)
- [Interactive instruments](#-interactive-instruments-used-in-this-lab)
- [What to observe](#-what-to-observe)
- [Completion criteria](#-completion-criteria)
- [Reflection questions](#-reflection-questions)
- [What this unlocks](#-what-this-unlocks)
- [Next lab](#-next-lab)
- [Notes for educators](#-notes-for-educators)

---

## Core concept

**Identity in Web3 is cryptographic and network-agnostic — but trust is defined by the network you join.**

In this lab, you explore how wallets, cryptographic keys, and addresses form the basis of identity in a permissioned Ethereum network based on Hyperledger Besu.

---

## 🎯 Learning objectives

- Explain the role of **private keys**, **public keys**, and **addresses** in Web3 identity.
- Understand what a **wallet** is in a **permissioned blockchain**.
- Describe how identity exists **before** transactions or smart contracts.

---

## 🧠 Prerequisites

- Modern web browser (Chrome / Firefox / Brave)
- Browser wallet (MetaMask or equivalent)
- Besu Edu‑Net RPC details (provided by instructor)

---

## 🧩 Conceptual background (read carefully)

### Identity, Address, and Network Context

![Wallet, address, and network context](./diagrams/lab01-identity-network.png)

Traditional systems rely on accounts and passwords.

Web3 systems rely on:
- cryptographic key pairs
- locally controlled wallets
- network‑level trust

A wallet is:

> A local cryptographic tool that manages keys and signs messages for a specific blockchain network.

---

## 🛠️ Environment

- **Network:** Besu Edu‑Net (permissioned QBFT)
- **Transactions:** Not required
- **Gas:** Not required

---

## 🧪 Lab steps

### Step 1 — Configure your wallet for Besu Edu‑Net

Add Besu Edu‑Net as a custom network and switch to it.

### Step 2 — Create or select a wallet account

Ensure your wallet is connected and note your public address.

### Step 3 — Inspect your address

Observe format, length, and checksum casing.

### Step 4 — Understand the key relationship

Private key → Public key → Address (one‑way derivation).

### Step 5 — Identity without accounts

You have identity without usernames or passwords.

---

## 🧰 Interactive instruments used in this lab

This lab uses a set of standalone, read‑only Web3Edu lab tools
designed to help students build a correct mental model of identity
and network context in Web3 systems.

---

### 🔧 Instrument A — Network Identifier
Identify which blockchain network your wallet is currently operating on.

- Detects the active `chainId`
- Distinguishes between Ethereum, testnets, and Besu‑based networks
- Demonstrates that wallet identity persists across networks

*(Provided via the web3edu‑lab‑tools repository)*

---

### 🔧 Instrument B — Address Anatomy
Visual inspection of Ethereum address structure.

- Prefix, body length, and checksum casing
- One‑way derivation from public keys
- Textual representations vs on‑chain identity

*(Provided via the web3edu‑lab‑tools repository)*

---

### 🔧 Instrument C — Identity Scope Visualizer
Explore how the same wallet address represents different meanings
across blockchain networks.

- Same address, different balances
- Identity vs context separation
- Network‑defined trust

*(Provided via the web3edu‑lab‑tools repository)*

---

## 🔍 What to observe

- Identity exists before transactions
- Wallets control keys locally
- Networks define trust

---

## ✅ Completion criteria

- [ ] Wallet connected to Besu Edu‑Net
- [ ] Public address identified
- [ ] Explain private key ownership

---

## 🧠 Reflection questions

1. Why does Web3 identity not require accounts?
2. What happens if a private key is leaked?
3. Why use a permissioned Besu network here?

---

## 🎁 What this unlocks

- Message signing
- Ownership proofs
- Access‑controlled contracts

---

## 🧭 Next lab

➡️ **Lab 02 — Message Signing & Ownership**

---

## 🇬🇷 Ελληνικά

## Κεντρική Έννοια

**Η ταυτότητα στο Web3 είναι κρυπτογραφική και ανεξάρτητη δικτύου — η εμπιστοσύνη όμως καθορίζεται από το δίκτυο.**

Σε αυτό το εργαστήριο εξετάζετε πώς πορτοφόλια, κλειδιά και διευθύνσεις αποτελούν τη βάση της ταυτότητας σε ένα αδειοδοτημένο Ethereum δίκτυο (Hyperledger Besu).

---

## 🎯 Μαθησιακοί στόχοι

- Κατανόηση ρόλου ιδιωτικού και δημόσιου κλειδιού
- Κατανόηση έννοιας πορτοφολιού
- Κατανόηση ταυτότητας πριν από συναλλαγές

---

## 🧠 Προαπαιτούμενα

- Σύγχρονος browser
- Πορτοφόλι (π.χ. MetaMask)
- Στοιχεία πρόσβασης στο Besu Edu‑Net

---

## 🧩 Εννοιολογικό υπόβαθρο

Στο Web3:
- δεν υπάρχουν λογαριασμοί
- δεν υπάρχουν κωδικοί
- η ταυτότητα βασίζεται σε κλειδιά

Το πορτοφόλι είναι:

> Ένα τοπικό εργαλείο που διαχειρίζεται κρυπτογραφικά κλειδιά και υπογράφει μηνύματα.

---

## 🛠️ Περιβάλλον

- **Δίκτυο:** Besu Edu‑Net
- **Συναλλαγές:** Όχι
- **Gas:** Όχι

---

## 🧪 Βήματα εργαστηρίου

### Βήμα 1 — Ρύθμιση πορτοφολιού

Προσθέστε το Besu Edu‑Net και συνδεθείτε.

### Βήμα 2 — Επιλογή λογαριασμού

Εντοπίστε τη δημόσια διεύθυνσή σας.

### Βήμα 3 — Παρατήρηση διεύθυνσης

Μορφή, μήκος, checksum.

### Βήμα 4 — Σχέση κλειδιών

Ιδιωτικό → Δημόσιο → Διεύθυνση.

### Βήμα 5 — Ταυτότητα χωρίς λογαριασμούς

Η ταυτότητα υπάρχει χωρίς εγγραφή.

---

## 🧰 Διαδραστικά εργαλεία

Το εργαστήριο χρησιμοποιεί ένα σύνολο αυτόνομων, μόνο για ανάγνωση
εργαλείων Web3Edu, σχεδιασμένων ώστε να βοηθούν τους φοιτητές
να διαμορφώσουν ένα σωστό νοητικό μοντέλο ταυτότητας
και πλαισίου λειτουργίας στα Web3 συστήματα.

---

### 🔧 Εργαλείο A — Αναγνώριση Δικτύου (Network Identifier)
Αναγνώριση του blockchain δικτύου στο οποίο λειτουργεί το πορτοφόλι.

- Εντοπισμός του ενεργού `chainId`
- Διάκριση μεταξύ Ethereum, testnets και Besu δικτύων
- Κατανόηση ότι η ταυτότητα πορτοφολιού παραμένει ίδια σε όλα τα δίκτυα

*(Παρέχεται μέσω του αποθετηρίου web3edu‑lab‑tools)*

---

### 🔧 Εργαλείο B — Ανατομία Διεύθυνσης (Address Anatomy)
Οπτική ανάλυση της δομής μιας διεύθυνσης Ethereum.

- Πρόθεμα, μήκος, checksum χαρακτήρων
- Μονόδρομη παραγωγή από δημόσιο κλειδί
- Κειμενικές αναπαραστάσεις και ταυτότητα blockchain

*(Παρέχεται μέσω του αποθετηρίου web3edu‑lab‑tools)*

---

### 🔧 Εργαλείο C — Οπτικοποίηση Πεδίου Ταυτότητας (Identity Scope)
Εξερεύνηση του τρόπου με τον οποίο η ίδια διεύθυνση
αποκτά διαφορετικό νόημα σε διαφορετικά blockchain δίκτυα.

- Ίδια διεύθυνση, διαφορετικά υπόλοιπα
- Διαχωρισμός ταυτότητας και πλαισίου
- Η εμπιστοσύνη καθορίζεται από το δίκτυο

*(Παρέχεται μέσω του αποθετηρίου web3edu‑lab‑tools)*

---

## 🔍 Τι να παρατηρήσετε

- Η ταυτότητα προηγείται των συναλλαγών
- Το δίκτυο καθορίζει εμπιστοσύνη

---

## 🧠 Ερωτήσεις αναστοχασμού

1. Γιατί δεν χρειάζονται λογαριασμοί στο Web3;
2. Τι συμβαίνει αν διαρρεύσει το ιδιωτικό κλειδί;

---

## 🎁 Τι ξεκλειδώνει

- Υπογραφή μηνυμάτων
- Απόδειξη ιδιοκτησίας

---

© Web3Edu
