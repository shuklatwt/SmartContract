 🧮 Counter Smart Contract

A simple smart contract that implements a basic counter functionality with the ability to increment, decrement, and reset its value.

---

## 🪧 Project Overview

The **Counter Smart Contract** is a minimal Solidity project demonstrating how to manage and update state variables on-chain.
It serves as a foundational example for developers exploring **Flow EVM Testnet** and learning how to deploy, interact with, and test Ethereum-compatible smart contracts.

---

## 🌐 Network Details

* **Built on:** [Flow EVM Testnet](https://developers.flow.com/evm)
* **Contract Address:** `0xYourContractAddressHere`
  *(Replace with your deployed contract address once available.)*

---

## ⚙️ Tech Stack

| Component                | Description                                           |
| ------------------------ | ----------------------------------------------------- |
| **Solidity**             | Smart contract programming language                   |
| **Remix IDE / Hardhat**  | Development and deployment tools                      |
| **Flow EVM Testnet**     | EVM-compatible blockchain network used for deployment |
| **MetaMask**             | Wallet for managing testnet accounts and transactions |
| **EtherScan (FlowScan)** | Explorer for verifying deployed contracts             |

---

## 🧾 Smart Contract

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract Counter {
    uint256 public count;

    function getCount() public view returns (uint256) {
        return count;
    }

    function increment() public {
        count += 1;
    }

    function decrement() public {
        require(count > 0, "Counter cannot go below zero");
        count -= 1;
    }

    function reset() public {
        count = 0;
    }
}
```

---

## 🚀 Deployment (Remix IDE - Flow EVM Testnet)

1. Open [Remix IDE](https://remix.ethereum.org/).
2. Create a file named `Counter.sol` and paste the code above.
3. Go to the **Solidity Compiler** tab and compile the contract (version `0.8.x`).
4. In **Deploy & Run Transactions**, set the **Environment** to “Injected Provider - MetaMask”.
5. Connect your MetaMask wallet to **Flow EVM Testnet**.
6. Click **Deploy** and copy your deployed **contract address**.

---

## 🧠 How It Works

* `count` → A state variable storing the counter value.
* `increment()` → Increases the counter by one.
* `decrement()` → Decreases the counter by one (checks if `count > 0`).
* `reset()` → Resets the counter to zero.
* `getCount()` → Returns the current count value.

---

## 🔮 Future Improvements

* Add **event emitters** for `Incremented`, `Decremented`, and `Reset`.
* Introduce **access control** (only owner can modify counter).
* Implement **batch operations** or **multi-user counters**.
* Build a simple **frontend (React + Ethers.js)** to interact with the contract visually.
* Store and visualize transaction history on-chain.

---

## 🪪 License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).

---

Would you like me to add a **“Frontend Integration Guide”** section (showing how to connect and interact with this contract using `ethers.js` on Flow EVM Testnet)?
