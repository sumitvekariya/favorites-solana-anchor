# Building Your First Solana Smart Contract with Anchor: Chapter 1

This project is a beginner-friendly introduction to building Solana smart contracts using the **Anchor framework**. It is based on **Chapter 1** of the [Solana Developer Bootcamp 2024](https://sumitvekariya7.medium.com/building-your-first-solana-smart-contract-with-anchor-chapter-1-fd585ff21651). The goal is to create a decentralized application (dApp) that allows users to store and update their favorite things on the blockchain.

---

## **Introduction**

The blockchain revolution is here, and Solana is leading the charge with its high-speed, low-cost transactions. This project demonstrates how to:
1. Save user-specific data (favorite number, color, and hobbies) on the blockchain.
2. Update the saved data securely.
3. Ensure only the owner of the data can modify it.

We achieve this using **Program Derived Addresses (PDAs)**, which act as a key-value store for Solana programs. The project is built using the **Anchor framework**, which simplifies Solana development with safe defaults, macros, and predefined structures.

---

## **Features**

- **Store User Data**: Save a user's favorite number, color, and hobbies on the blockchain.
- **Update Data**: Allow users to update their saved data.
- **Data Ownership**: Ensure only the owner of the data can modify it using PDAs.
- **Anchor Framework**: Leverage Anchor for simplified Solana development.

---

## **Prerequisites**

Before you begin, ensure you have the following installed:

1. **Rust**: Install Rust from [rust-lang.org](https://www.rust-lang.org/).
2. **Solana CLI**: Install the Solana CLI from [docs.solana.com](https://docs.solana.com/cli/install-solana-cli-tools).
3. **Anchor CLI**: Install the Anchor framework by following the instructions [here](https://book.anchor-lang.com/chapter_2/installation.html).
4. **Node.js**: Install Node.js from [nodejs.org](https://nodejs.org/).

---

## **Installation**

Follow these steps to set up the project:

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. Install dependencies:
   ```bash
   anchor install
   ```

3. Build the project:
   ```bash
   anchor build
   ```

4. Deploy the program to a local Solana cluster:
   ```bash
   anchor deploy
   ```

5. Start the Solana local validator:
   ```bash
   solana-test-validator
   ```

---

## **Usage**

1. **Run the Client**: Use the provided client code to interact with the deployed program.
2. **Save Data**: Call the `save_data` function to store your favorite number, color, and hobbies.
3. **Update Data**: Use the `update_data` function to modify your saved information.
4. **Verify Ownership**: Only the wallet that created the data can update it.

---

## **Code Explanation**

### **1. Program Derived Addresses (PDAs)**
PDAs are used to uniquely store user data. They are derived from:
- The user's wallet address.
- A predefined seed (e.g., "user_data").

This ensures that each user's data is tied to their wallet and cannot be accessed or modified by others.

### **2. Anchor Framework**
The Anchor framework simplifies Solana development by:
- Providing macros to define program logic.
- Managing accounts and data storage safely.
- Offering predefined structures for account handling.

### **3. Smart Contract Logic**
The smart contract includes:
- **Initialization**: Creates a PDA for the user and stores their data.
- **Update Function**: Allows the user to update their data if they are the owner.

---

## **Testing**

To test the program:

1. Run the local Solana validator:
   ```bash
   solana-test-validator
   ```

2. Deploy the program:
   ```bash
   anchor deploy
   ```

3. Use the provided test scripts to interact with the program:
   ```bash
   anchor test
   ```

4. Verify the results on the local blockchain.

---

## **Resources**

- **Full Blog Post**: [Building Your First Solana Smart Contract with Anchor: Chapter 1](https://sumitvekariya7.medium.com/building-your-first-solana-smart-contract-with-anchor-chapter-1-fd585ff21651)
- **Solana Playground**: [Try it out here](https://beta.solpg.io/https://sumitvekariya7.medium.com/building-your-first-solana-smart-contract-with-anchor-chapter-1-fd585ff21651)
- **Anchor Framework Documentation**: [Anchor Book](https://book.anchor-lang.com/)
- **Solana Documentation**: [Solana Docs](https://docs.solana.com/)

---

## **Contributing**

Contributions are welcome! If you find any issues or have suggestions for improvement, feel free to open an issue or submit a pull request.

---

## **License**

This project is licensed under the MIT License. See the `LICENSE` file for details.
