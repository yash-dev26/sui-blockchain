# 🎴 Sui Loyalty Card DApp

A full-stack decentralized application (DApp) built on the Sui blockchain that allows users to mint and manage loyalty card NFTs. **This project was developed during a blockchain workshop that covered blockchain fundamentals and Sui development.**

## 📚 What I Learned

This project demonstrates key concepts learned during the blockchain workshop:

- **Blockchain Fundamentals**: Understanding decentralized systems, consensus mechanisms, and smart contracts
- **Sui Move Language**: Writing secure smart contracts using Move's ownership model
- **DApp Architecture**: Building full-stack blockchain applications with React frontends
- **NFT Concepts**: Creating and managing non-fungible tokens on Sui
- **Wallet Integration**: Connecting web applications to blockchain wallets

## 🚀 Features

- **Mint Loyalty Cards**: Create unique NFT loyalty cards with custom metadata
- **Wallet Integration**: Connect and interact with Sui wallets
- **Smart Contract**: Secure Move contract with admin capabilities
- **Responsive UI**: Clean React interface for easy interaction
- **Transaction Handling**: Real-time transaction processing and feedback

## 🛠️ Tech Stack

### Backend (Blockchain)
- **Sui Move**: Smart contract development language
- **Sui Framework**: Built-in libraries for objects, transfers, and more
- **Package Management**: Move.toml for dependency management

### Frontend (Web Interface)
- **React 19**: Modern React with hooks
- **Sui DApp Kit**: Official Sui wallet integration
- **TanStack Query**: Data fetching and state management
- **CSS3**: Responsive styling

## 📁 Project Structure

```
loyalty_card/
├── sources/                    # Move smart contracts
│   ├── loyalty_card.move      # Main contract logic
│   └── tests/                 # Contract tests
├── frontend/                  # React DApp
│   ├── src/
│   │   ├── App.js            # Main application component
│   │   ├── App.css           # Styling
│   │   └── index.js          # React entry point
│   └── public/               # Static assets
├── build/                    # Compiled Move bytecode
├── Move.toml                 # Move package configuration
└── README.md                 # This file
```

## 🏃‍♂️ Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v16 or higher)
- [Sui CLI](https://docs.sui.io/build/install) installed
- A Sui wallet (Sui Wallet browser extension recommended)

### Installation

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd loyalty_card
   ```

2. **Build the Move contract**
   ```bash
   sui move build
   ```

3. **Install frontend dependencies**
   ```bash
   cd frontend
   npm install --legacy-peer-deps
   ```

4. **Start the development server**
   ```bash
   npm start
   ```

5. **Open your browser**
   Navigate to `http://localhost:3000`

## 📖 How to Use

### 1. Deploy the Contract

First, deploy your Move contract to Sui:

```bash
sui client publish --gas-budget 50000000
```

Copy the Package ID from the deployment output.

### 2. Connect Your Wallet

1. Install the Sui Wallet browser extension
2. Create or import a wallet
3. Get some test SUI tokens from the faucet
4. Click "Connect" button in the DApp

### 3. Mint Loyalty Cards

1. Enter the Package ID from your deployment
2. Fill in the customer's Sui address
3. Add an image URL for the loyalty card
4. Click "Mint your NFT"
5. Confirm the transaction in your wallet

## 🎯 Smart Contract Details

### Core Functions

- **`init()`**: Initializes the contract and creates admin capability
- **`mint_loyalty()`**: Mints a new loyalty card NFT

### Data Structures

```move
public struct Loyalty has key, store {
    id: UID,
    customer_id: address,
    image_url: String
}

public struct AdminCap has key, store {
    id: UID
}
```

## 🧪 Testing

Run the Move contract tests:

```bash
sui move test
```

## 🌐 Deployment Networks

This DApp can be deployed on:

- **Sui Devnet**: For development and testing
- **Sui Testnet**: For staging and pre-production
- **Sui Mainnet**: For production deployment

## 🛡️ Security Features

- **Ownership Model**: Sui's ownership system prevents double-spending
- **Admin Capabilities**: Protected functions using capability-based security
- **Type Safety**: Move's type system prevents common smart contract bugs

## 🔗 Useful Links

- [Sui Documentation](https://docs.sui.io/)
- [Move Language Guide](https://move-book.com/)
- [Sui DApp Kit](https://sdk.mystenlabs.com/dapp-kit)
- [Sui Explorer](https://explorer.sui.io/)

## 🎓 Learning Outcomes

Through building this project, I gained hands-on experience with:

- **Smart Contract Development**: Writing secure, efficient Move contracts
- **DApp Architecture**: Understanding how frontends interact with blockchains
- **Wallet Integration**: Implementing wallet connectivity and transaction signing
- **NFT Standards**: Creating and managing digital assets on Sui
- **Testing & Deployment**: Full development lifecycle on blockchain

## 🤝 Contributing

This is a learning project, but feel free to:

1. Fork the repository
2. Create a feature branch
3. Make your improvements
4. Submit a pull request

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- Blockchain workshop instructors for the foundational knowledge
- Sui Foundation for excellent documentation and tools
- Move language designers for creating a secure smart contract language
- The blockchain community for inspiration and support

---

**Happy Building! 🚀**

*Built with ❤️ using Sui Move and React*