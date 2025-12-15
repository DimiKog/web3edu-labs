🧪 Lab 01 — Wallets, Keys & Web3 Identity (Besu Edu-Net)

Core Concept

Identity in Web3 is cryptographic and network-agnostic — but trust is defined by the network you join.

In this lab, you will explore how wallets, cryptographic keys, and addresses form the basis of identity in a permissioned Ethereum network based on Hyperledger Besu.

⸻

🎯 Learning Objectives

After completing this lab, you will be able to:
	•	Explain the role of private keys, public keys, and addresses in Web3 identity
	•	Understand what a wallet is in the context of a private / permissioned blockchain
	•	Describe how identity exists before any transaction or smart contract

⸻

🧠 Prerequisites
	•	A modern web browser (Chrome / Firefox / Brave)
	•	A browser wallet (e.g. MetaMask)
	•	Access details for the Besu Edu-Net RPC endpoint (provided by the instructor)

No prior Web3 or blockchain experience is required.

⸻

🧩 Conceptual Background (Read Carefully)

In traditional systems:
	•	Identity is managed by accounts
	•	Authentication relies on usernames & passwords
	•	A central authority controls access

In Web3 systems:
	•	Identity is based on cryptographic key pairs
	•	Ownership is proven using private keys
	•	Trust is established by joining a specific network

In this course, the network is Besu Edu-Net, a permissioned Ethereum network operated for educational and research purposes.

A wallet is not:
	•	an online account
	•	a database
	•	a balance holder

A wallet is:

A local cryptographic tool that manages keys and signs messages for a specific blockchain network.

⸻

🛠️ Environment
	•	Blockchain network: Besu Edu-Net (QBFT / permissioned)
	•	Tools:
	•	Browser wallet (MetaMask or equivalent)
	•	Blockchain interaction:
	•	No transactions required
	•	No gas required for this lab

⸻

🧪 Lab Steps

Step 1 — Configure Your Wallet for Besu Edu-Net
	1.	Open your browser wallet
	2.	Add a custom network using the details provided by the instructor:
	•	Network Name: Besu Edu-Net
	•	RPC URL: (provided separately)
	•	Chain ID: (provided separately)
	•	Currency Symbol: EDU (or as defined)
	3.	Switch your wallet to Besu Edu-Net

📌 This step explicitly binds your identity to this network.

⸻

Step 2 — Create or Select a Wallet Account
	1.	Create a new wallet account or select an existing one
	2.	Ensure the wallet is connected to Besu Edu-Net
	3.	Locate your public address

⚠️ Never share:
	•	your private key
	•	your seed phrase

⸻

Step 3 — Inspect Your Address
	1.	Copy your wallet address
	2.	Observe:
	•	hexadecimal format
	•	fixed length
	•	checksum casing (if present)
	3.	Note:
	•	the address is public
	•	it does not reveal the private key
	•	it uniquely represents you on this network

⸻

Step 4 — Understand the Key Relationship

Reflect on the following facts:
	•	The private key proves ownership
	•	The public key is mathematically derived from the private key
	•	The address is derived from the public key
	•	This derivation is one-way

➡️ No one can derive your private key from your address.

⸻

Step 5 — Identity Without Accounts

Consider the following:
	•	You did not register with Besu Edu-Net
	•	You did not create a username
	•	You did not set a password

Yet:
	•	You have a valid on-chain identity
	•	You fully control it
	•	The network can verify your actions cryptographically

This is the foundation of self-sovereign identity.

⸻

🔍 What to Observe
	•	Identity exists before transactions and smart contracts
	•	Wallets manage keys locally, not on the network
	•	The same wallet software can connect to different networks, but identity is network-scoped

⸻

✅ Completion Criteria

This lab is complete when you can:
	•	Connect your wallet to Besu Edu-Net
	•	Identify your public address on this network
	•	Explain the role of private keys in identity and ownership

No transaction submission is required.

⸻

🧠 Reflection Questions

Answer briefly:
	1.	Why does Web3 identity not require user accounts?
	2.	What would happen if your private key was leaked?
	3.	Why is it important that this lab runs on a permissioned Besu network instead of a public testnet?
