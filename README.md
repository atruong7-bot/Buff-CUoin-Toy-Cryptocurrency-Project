
# Buff-CUoin: Toy Cryptocurrency Project

## Overview

Buff-CUoin is a blockchain-based toy cryptocurrency system implemented in C++ for educational purposes. This project was developed as part of **CSCI 2270: Data Structures** to demonstrate key principles of blockchain technology, including transactions, blocks, mining, and verification.

## Features

- **Transactions**: Users can send Buff-CUoins (BFC) between accounts.
- **Mining**: Blocks are mined through a proof-of-work algorithm, and miners are rewarded with BFC for successfully mining a block.
- **Blockchain Verification**: Validates the integrity of the blockchain by ensuring that each block links correctly with the previous one.
- **Balance Checking**: Users can query the balance of any account.
- **Blockchain Visualization**: The system allows users to view the blockchain, including block hashes, transactions, and timestamps.

## File Structure

- **`Block.hpp`**: Header file defining the `Block` class, which represents a block in the blockchain.
- **`Block.cpp`**: Implementation of the `Block` class, including functions for mining and hashing.
- **`Blockchain.hpp`**: Header file defining the `Blockchain` class, which manages the entire chain of blocks and handles transactions.
- **`Blockchain.cpp`**: Implementation of the `Blockchain` class, including functions for adding transactions, mining, and verifying the chain.
- **`sha256.hpp`**: Header file for the SHA-256 hash algorithm used to secure the blockchain.
- **`sha256.cpp`**: Implementation of the SHA-256 algorithm, used in the mining process.
- **`Transaction.hpp`**: Header file defining the `Transaction` class, which represents a single transaction between two parties.
- **`Transaction.cpp`**: Implementation of the `Transaction` class, including functions for creating and managing transactions.
- **`a.out`**: Compiled executable file for running the project.
- **`CSCI2270_Spring22_Project.pdf`**: Project description and specifications.

## How to Compile

To compile the project, use the following commands:

```bash
g++ -std=c++17 Blockchain.cpp Block.cpp Transaction.cpp sha256.cpp -o BuffCUoin
```

This will compile the source files and produce an executable named `BuffCUoin`.

## How to Run

After compiling, run the program with:

```bash
./BuffCUoin
```

This will start the text-based interface that allows you to interact with the blockchain.

## User Interface

The system provides a simple text-based interface with the following options:

1. **Add a Transaction**: Create a transaction between two users.
2. **Verify Blockchain**: Check if the blockchain is valid.
3. **Mine Pending Transactions**: Mine a new block and receive rewards.
4. **Visualize Blockchain**: Print details of the entire blockchain.
5. **Get Balance of a User**: Display the balance of a specific user.
6. **Quit**: Exit the program.

## Program Structure

- **Block Class**:
  - Manages individual blocks of the blockchain.
  - Contains the `nonce`, `previousHash`, `timestamp`, and a list of transactions.
  - Includes the `mineBlock()` function that implements proof-of-work.

- **Blockchain Class**:
  - Manages the list of blocks (the chain).
  - Includes functionality for adding transactions, mining, and checking the balance of users.
  - Provides a function to verify the integrity of the entire chain.

- **Transaction Class**:
  - Represents a single transaction between a sender and receiver.
  - Includes methods for creating and displaying transactions.

## Team Members

- Andrew Truong
- Blaise Como
