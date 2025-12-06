# Fund Me – Solidity Smart Contract (Cyfrin Course Project)

This repository contains my implementation of the **Fund Me** smart contract, developed as part of the  
**Solidity Smart Contract Development** course by **Cyfrin**.

The project helped me understand the fundamentals of real-world smart contract development, including  
data structures, price feeds, libraries, security patterns, and gas optimizations.

---

## 🚀 Project Overview

Fund Me is a decentralized funding contract where users can send ETH, and only the contract owner  
can withdraw the balance. To prevent extremely small transactions, the contract uses a minimum  
USD threshold based on **Chainlink Price Feeds**.

---

## 📚 What I Learned

### ✔ Solidity Core Concepts
- State variables, immutables, and constants  
- Mappings & arrays  
- Modifiers and custom errors  
- Function visibility & fallback/receive functions  
- Working with `msg.value`, `msg.sender`, and calldata/memory/storage

### ✔ Working with Chainlink Oracles
- Using `AggregatorV3Interface`  
- Reading real-time ETH/USD price feeds  
- Understanding decentralized oracles

### ✔ Writing and Using Libraries
- Creating a custom **PriceConverter** library  
- Extending uint256 using `using PriceConverter for uint256;`  
- Keeping the code modular and reusable

### ✔ Security & Best Practices
- Owner-only functions (`onlyOwner` modifier)  
- Proper ETH withdrawal pattern  
- Gas optimizations with **constant** and **immutable**

### ✔ Deployment Experience
I deployed this contract on **zkSync Testnet**, gaining hands-on experience with:
- Configuring RPC  
- Deploying & verifying contracts  
- Testing interactions using a Web3 wallet

---

## 🧩 Files in This Repo
- `FundMe.sol` → Main contract  
- `PriceConverter.sol` → Custom price conversion library  
- (Any additional helper files)

---

## 🛠 Tech Stack
- Solidity ^0.8.18  
- Chainlink Price Feeds  
- zkSync Testnet  
- Remix IDE

---

## 💡 How It Works
1. Users call `fund()` and send ETH.  
2. Contract checks if the value ≥ **$5 USD** using live Chainlink price data.  
3. Owner can call `withdraw()` to transfer all funds securely.  
4. Every funding event is recorded on-chain.

---

## 📬 Contact
If you want to discuss Solidity, Web3, zkSync, or decentralized apps — feel free to connect!

