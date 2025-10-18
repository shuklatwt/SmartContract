🧮 Counter Smart Contract

A simple Solidity smart contract that implements a basic counter with increment, decrement, and reset functionalities.

---

## 📋 Overview

The **Counter** contract demonstrates fundamental concepts of Solidity, such as:

* State variables
* Public visibility
* Functions
* `require` statements for validation

It can be used as a beginner-friendly example to understand how smart contracts store and modify data on the Ethereum blockchain.

---

## ⚙️ Features

* **Increment:** Increase the counter by 1
* **Decrement:** Decrease the counter by 1 (cannot go below zero)
* **Reset:** Set the counter back to zero
* **Get Count:** Retrieve the current count value

---

## 🧾 Contract Code

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

## 🚀 Deployment (Using Remix IDE)

1. Go to [Remix Ethereum IDE](https://remix.ethereum.org/).
2. Create a new file named `Counter.sol`.
3. Paste the contract code above.
4. Compile the contract using the **Solidity Compiler** (version `0.8.x`).
5. Deploy the contract using the **Deploy & Run Transactions** tab.
6. Use the interface to call:

   * `increment()` → increase the count
   * `decrement()` → decrease the count
   * `reset()` → reset to 0
   * `count` or `getCount()` → view current count

---

## 🧠 Concepts Demonstrated

* **State variables** — Persistent storage on the blockchain
* **Function visibility** — `public`, `view`
* **Error handling** — `require()` to prevent invalid state changes
* **Gas efficiency** — Simple and optimized operations

---

## 🪪 License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).

---

Would you like me to make it look more **GitHub-ready** (with emojis, formatting, and a “Getting Started” section for Hardhat/Foundry setup)?
