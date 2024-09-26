---

# Buff-CUoin: A Simplified Blockchain Cryptocurrency

Buff-CUoin is a lightweight cryptocurrency project built to demonstrate the core principles of blockchain technology. It features a text-based blockchain system where users can create transactions, mine blocks, verify the blockchain's integrity, and check balances. The system is implemented in C++ and includes basic functionality such as proof-of-work mining, transaction handling, and blockchain validation.

## Key Features

- **Transaction Management**: Allows users to transfer Buff-CUoins (BFC) between accounts.
- **Blockchain Structure**: A linked list of blocks, each containing multiple transactions, a timestamp, and a cryptographic hash linking it to the previous block.
- **Proof-of-Work Mining**: Secures the blockchain by making the process of adding new blocks computationally challenging, rewarding successful miners with BFC.
- **Blockchain Validation**: Verifies that each block correctly references the previous block, ensuring the integrity of the entire chain.
- **Balance Checking**: Users can query their Buff-CUoin balance based on the history of the blockchain.
- **Readable Blockchain Printout**: Provides a human-readable printout of the entire blockchain, including transaction history and metadata for each block.

## How It Works

### Blockchain

The blockchain is a sequential list of blocks, where each block records multiple transactions. Each block includes:
- A list of pending transactions.
- The cryptographic hash of the previous block.
- A timestamp.
- A nonce value for mining.

### Mining

Mining is the process of securing the blockchain by solving a computational puzzle. Miners must find a nonce value that, when hashed along with the block's content, results in a hash with a specific number of leading zeros (proof-of-work). Upon successfully mining a block, the miner receives a reward in Buff-CUoins.

### Transactions

Transactions involve a sender, a receiver, and a specified amount of Buff-CUoins. The system verifies that the sender has sufficient balance before allowing the transaction to proceed. Valid transactions are stored in a pool of pending transactions until they are included in a mined block.

## Getting Started

### Prerequisites

You'll need a C++17-compatible compiler to build and run the project.

### Build Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/BuffCUoin.git
   cd BuffCUoin
   ```

2. Compile the project:
   ```bash
   g++ -std=c++17 Blockchain.cpp Block.cpp Transaction.cpp sha256.cpp -o BuffCUoin
   ```

3. Run the executable:
   ```bash
   ./BuffCUoin
   ```

### Usage

Once you run the program, you will be presented with a simple command-line interface that allows you to interact with the blockchain. Here are the options you can choose from:

1. **Add a Transaction**: Record a transaction between a sender and a receiver, specifying the amount of Buff-CUoins.
2. **Verify Blockchain**: Ensure that the blockchain's integrity is intact by checking the hash links between blocks.
3. **Mine Pending Transactions**: Mine a block containing all pending transactions and receive a mining reward.
4. **Visualize Blockchain**: View a detailed breakdown of all blocks in the blockchain, including transaction histories and metadata.
5. **Get Balance of a User**: Check how many Buff-CUoins a user has based on their transaction history.
6. **Quit**: Exit the program.

### Example Interaction

```bash
======Main Menu======
1. Add a transaction
2. Verify Blockchain
3. Mine Pending Transactions
4. Visualize Blockchain
5. Get Balance of User
6. Quit
```

### Adding a Transaction

You’ll be prompted to enter the sender, receiver, and amount for each transaction. Pending transactions will remain in the pool until a new block is mined.

### Mining

Once you initiate mining, the program will find a valid nonce that satisfies the proof-of-work condition. The miner receives a reward in Buff-CUoins for successfully mining a block.

### Checking Blockchain Validity

Blockchain integrity is verified by ensuring that each block's hash matches the previous block's reference and that the proof-of-work conditions are met.

### Viewing the Blockchain

You can view the entire blockchain, including transaction details, block hashes, timestamps, and nonce values for each block.

## Project Structure

- **`Block.cpp`**: Handles the core functionality of individual blocks, including hashing and mining.
- **`Blockchain.cpp`**: Manages the blockchain, processes transactions, and handles block mining.
- **`Transaction.cpp`**: Defines how transactions between users are created and managed.
- **`sha256.cpp`**: Provides a cryptographic hash function used to secure the blockchain.

## Technical Details

Buff-CUoin leverages the SHA-256 cryptographic hash function to secure blocks in the blockchain. Mining difficulty can be adjusted by modifying the number of leading zeros required in the block hash.

The system currently uses an in-memory data structure, meaning that the blockchain exists only for the duration of program execution. Further development could include reading from and writing to a file for persistence.

## Authors

- **Andrew Truong**
- **Blaise Como**

---
