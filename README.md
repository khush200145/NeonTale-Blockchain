# ⛓️ NeonTale Blockchain

A Python-based blockchain project built using **Flask** to explore the fundamental concepts of blockchain technology, proof-of-work mining, transactions, and decentralized networks.

NeonTale demonstrates how multiple blockchain nodes can communicate, share transactions, mine blocks, and maintain a distributed ledger.

## 🚀 Features

- **Blockchain Creation:** Creates a blockchain with a genesis block and maintains a chain of blocks.
- **Proof of Work (PoW):** Implements a mining algorithm that finds a valid proof by satisfying a SHA-256 hash condition.
- **Transaction Management:** Allows users to add transactions containing sender, receiver, and amount information.
- **Block Mining:** Mines new blocks and includes pending transactions in the blockchain.
- **Blockchain Validation:** Checks the integrity of the chain by validating block hashes and proof of work.
- **Multiple Nodes:** Demonstrates a network of three blockchain nodes running on different ports.
- **Node Connection:** Allows nodes to connect and discover other nodes in the network.
- **Consensus Mechanism:** Demonstrates chain replacement to synchronize nodes with a valid, longer blockchain.

## 🛠️ Tech Stack

- **Language:** Python
- **Web Framework:** Flask
- **Hashing Algorithm:** SHA-256
- **HTTP Requests:** Requests
- **API Testing:** Postman
- **Development Environment:** Anaconda / Spyder
- **Version Control:** Git and GitHub

## 📂 Project Structure

The project contains three Python files representing three blockchain nodes.

```text
NeonTale-Blockchain/
│
├── neontalecoin.py       # Blockchain node 1
├── neontalecoin2.py      # Blockchain node 2
├── neontalecoin3.py      # Blockchain node 3
│
└── README.md
```

*Note: Adjust the filenames above if your actual files use different names.*

## ⚙️ Installation and Setup

### 1. Clone the repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd NeonTale-Blockchain
```

Replace the repository URL with your GitHub repository URL.

### 2. Install the dependencies

Make sure Python is installed, then run:

```bash
pip install flask requests
```

### 3. Run the blockchain nodes

Open three separate terminals or run the three files in separate Spyder consoles.

```bash
python neontalecoin.py
```

```bash
python neontalecoin2.py
```

```bash
python neontalecoin3.py
```

Each node must use a different port number in its Flask configuration. Ensure the port numbers in your files match the URLs you use to access the nodes.

## 🔗 API Endpoints

The following endpoints represent the core operations demonstrated by the project. Check your source code for the exact endpoint names and HTTP methods.

| Endpoint | Purpose |
|---|---|
| `/get_chain` | Retrieves the blockchain and its blocks. |
| `/mine_block` | Performs proof-of-work mining and creates a new block. |
| `/is_valid` | Checks whether the blockchain is valid. |
| `/add_transaction` | Adds a transaction to the pending transaction list. |
| `/connect_node` | Registers other blockchain nodes in the network. |
| `/replace` | Checks and replaces the current chain when a valid, longer chain is available. |

## 🧪 Testing with Postman

You can test the blockchain API using Postman.

1. Start all three blockchain nodes.
2. Send requests to each node using its configured port.
3. Connect the nodes by submitting the other nodes' addresses.
4. Add transactions by sending the required JSON data.
5. Mine a block to include pending transactions.
6. Retrieve the blockchain to inspect the newly created block.
7. Validate the chain and test chain synchronization between nodes.

Example transaction payload:

```json
{
  "sender": "Alice",
  "receiver": "Bob",
  "amount": 10
}
```

Use the HTTP method expected by your implementation, typically `POST` for adding transactions and connecting nodes.

## 🔍 How It Works

1. **Genesis Block:** The blockchain starts with an initial block.
2. **Transactions:** New transactions are added to a pending transaction list.
3. **Mining:** The proof-of-work algorithm searches for a proof that satisfies the configured SHA-256 condition.
4. **Block Creation:** A successfully mined block stores the transactions, proof, timestamp, and previous block hash.
5. **Node Communication:** Nodes exchange information about other nodes and their respective chains.
6. **Chain Synchronization:** The replacement mechanism compares chains and can adopt a valid, longer chain.

## 🎯 Learning Outcomes

Through this project, I explored:

- Blockchain data structures and linked blocks.
- Cryptographic hashing using SHA-256.
- Proof-of-work mining.
- REST APIs using Flask.
- JSON-based communication between nodes.
- Multi-node blockchain networking.
- Blockchain validation and chain synchronization.
- API testing with Postman.

## 🔮 Future Improvements

- Add digital signatures for transaction authentication.
- Implement wallet addresses and public-private key cryptography.
- Introduce transaction verification and stronger validation rules.
- Persist blockchain data using a database.
- Improve consensus and peer discovery.
- Develop a frontend dashboard for viewing blocks and transactions.
- Add automated unit and integration tests.

## ⚠️ Disclaimer

NeonTale is an educational blockchain prototype intended for learning and experimentation. It is not a production-ready cryptocurrency or a secure financial system. Its proof-of-work, transaction validation, consensus, and networking mechanisms may require further improvements before real-world use.

## 👨‍💻 Author

**Kushal Gupta**

This project represents my hands-on exploration of blockchain development using Python, Flask, and multi-node communication.

If you find this project useful for learning blockchain fundamentals, feel free to explore the code and suggest improvements.
