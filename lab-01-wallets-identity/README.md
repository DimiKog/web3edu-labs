
# 🧪 Lab 01 — Wallets, Keys & Web3 Identity (Besu Edu-Net)

## Table of Contents

- [Core concept](#core-concept)
- [Learning objectives](#-learning-objectives)
- [Prerequisites](#-prerequisites)
- [Conceptual background](#-conceptual-background-read-carefully)
- [Environment](#-environment)
- [Lab steps](#-lab-steps)
  - [Step 1 — Configure your wallet for Besu Edu-Net](#step-1--configure-your-wallet-for-besu-edu-net)
  - [Step 2 — Create or select a wallet account](#step-2--create-or-select-a-wallet-account)
  - [Step 3 — Inspect your address](#step-3--inspect-your-address)
  - [Step 4 — Understand the key relationship](#step-4--understand-the-key-relationship)
  - [Step 5 — Identity without accounts](#step-5--identity-without-accounts)
- [What to observe](#-what-to-observe)
- [Completion criteria](#-completion-criteria)
- [Reflection questions](#-reflection-questions)
- [What this unlocks](#-what-this-unlocks)
- [Next lab](#-next-lab)
- [Notes for educators](#-notes-for-educators)
- [License](#license)

---

## Core concept

**Identity in Web3 is cryptographic and network-agnostic — but trust is defined by the network you join.**

In this lab, you will explore how wallets, cryptographic keys, and addresses form the basis of identity in a permissioned Ethereum network based on Hyperledger Besu.

---

## 🎯 Learning objectives

- Explain the role of **private keys**, **public keys**, and **addresses** in Web3 identity.
- Understand what a **wallet** is in the context of a **private / permissioned** blockchain.
- Describe how identity exists **before** any transaction or smart contract.

---

## 🧠 Prerequisites

- A modern web browser (Chrome / Firefox / Brave)
- A browser wallet (e.g. MetaMask)
- Access details for the Besu Edu-Net RPC endpoint (provided by the instructor)

No prior Web3 or blockchain experience is required.

---

## 🧩 Conceptual background (read carefully)

In traditional systems:

- Identity is managed by accounts
- Authentication relies on usernames & passwords
- A central authority controls access

In Web3 systems:

- Identity is based on cryptographic key pairs
- Ownership is proven using private keys
- Trust is established by joining a specific network

In this course, the network is Besu Edu-Net, a permissioned Ethereum network operated for educational and research purposes.

A wallet is:

> A local cryptographic tool that manages keys and signs messages for a specific blockchain network.

---

## 🛠️ Environment

- **Blockchain network:** Besu Edu-Net (QBFT / permissioned)
- **Tools:** Browser wallet (MetaMask or equivalent)
- **Blockchain interaction:** No transactions required; no gas required

---

## 🧪 Lab steps

### Step 1 — Configure your wallet for Besu Edu-Net

1. Open your browser wallet.
2. Add a **custom network** using the details provided by the instructor:
   - **Network Name:** Besu Edu-Net
   - **RPC URL:** *(provided separately)*
   - **Chain ID:** *(provided separately)*
   - **Currency Symbol:** EDU *(or as defined)*
3. Switch your wallet to **Besu Edu-Net**.

> 📌 This step explicitly binds your identity to this network.

### Step 2 — Create or select a wallet account

1. Create a new wallet account or select an existing one.
2. Ensure the wallet is connected to Besu Edu-Net.
3. Locate your public address.

> ⚠️ Never share:
> - your private key
> - your seed phrase

### Step 3 — Inspect your address

1. Copy your wallet address.
2. Observe:
   - hexadecimal format
   - fixed length
   - checksum casing (if present)
3. Note:
   - the address is public
   - it does not reveal the private key
   - it uniquely represents you on this network

### Step 4 — Understand the key relationship

Reflect on the following facts:

- The private key proves ownership
- The public key is mathematically derived from the private key
- The address is derived from the public key
- This derivation is one-way

➡️ No one can derive your private key from your address.

### Step 5 — Identity without accounts

Consider the following:

- You did not register with Besu Edu-Net
- You did not create a username
- You did not set a password

Yet:

- You have a valid on-chain identity
- You fully control it
- The network can verify your actions cryptographically

This is the foundation of self-sovereign identity.

---

## 🔍 What to observe

- Identity exists before transactions and smart contracts
- Wallets manage keys locally, not on the network
- The same wallet software can connect to different networks, but identity is network-scoped

---

## ✅ Completion criteria

- [ ] Connect your wallet to **Besu Edu-Net**.
- [ ] Identify your public address on this network.
- [ ] Explain the role of private keys in identity and ownership.

No transaction submission is required.

---

## 🧠 Reflection questions

1. Why does Web3 identity not require user accounts?
2. What would happen if your private key was leaked?
3. Why is it important that this lab runs on a permissioned Besu network instead of a public testnet?

---

## 🎁 What this unlocks

- Message signing on Besu Edu-Net (Lab 02)
- Ownership proofs without transactions
- Access-controlled smart contracts
- DAO participation within the Web3Edu ecosystem

---

## 🧭 Next lab

➡️ **Lab 02 — Message Signing & Ownership (Besu Edu-Net)**

You will use your wallet to prove ownership of your identity by signing messages verified on the Besu network.

---

## 📌 Notes for educators

- This lab:
  - requires no gas
  - requires no smart contracts
  - is ideal as the first lab in a Besu-based course
- Suitable for:
  - undergraduate courses
  - MSc programs
  - professional training
- Typical duration: **20–30 minutes**

---

## License

This lab is part of the **Web3Edu Labs** series.

© Web3Edu — Educational and non-commercial use permitted.
