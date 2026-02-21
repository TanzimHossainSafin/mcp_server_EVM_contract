# MCP Server for EVM Smart Contract

This repository contains a Model Context Protocol (MCP) server implementation for interacting with a Donation DApp smart contract on EVM-compatible blockchains.

## 📋 Description

This MCP server enables seamless interaction with a smart contract deployed on an EVM-compatible blockchain. It provides tools to send donations, view top donors, check balances, and manage contract interactions through the Model Context Protocol.

## 🚀 Features

- **Send Donations**: Interact with the smart contract to send donations
- **View Top Donor**: Query the contract to see the highest contributor
- **Check Balance**: Get the current contract balance
- **View Total Donations**: Retrieve the total amount of donations received
- **Withdraw Funds**: Withdraw funds from the contract (owner only)

## 🛠️ Tech Stack

- **TypeScript**: Primary programming language
- **Ethers.js v6**: Ethereum library for blockchain interactions
- **MCP SDK**: Model Context Protocol implementation
- **Zod**: Schema validation
- **dotenv**: Environment variable management

## 📦 Installation

1. Clone the repository:
```bash
git clone https://github.com/TanzimHossainSafin/mcp_server_EVM_contract.git
cd mcp_server_EVM_contract
```

2. Install dependencies:
```bash
npm install
```

3. Set up environment variables:
```bash
cp .env.example .env
```

4. Edit `.env` file with your credentials:
```env
PRIVATE_KEY="Your wallet private key"
URL_RPC="Your RPC URL (e.g., Infura, Alchemy, or local node)"
```

## 🔧 Configuration

The server is configured to interact with the following smart contract:
- **Contract Address**: `0x877D405A0c80253692CD3173f47167aa0511a337`
- **Network**: Configure via `URL_RPC` environment variable

### Smart Contract ABI

The server uses the following contract functions:
- `donation_recieve(uint256)`: Send donations
- `withdraw()`: Withdraw funds
- `getBalance()`: Get contract balance
- `getTotalDonation()`: Get total donations
- `top_Donner_Donation()`: Get top donor details

## 🏃 Usage

### Build the project:
```bash
npm run build
```

### Start the MCP server:
```bash
npm start
```

### Available MCP Tools

#### 1. Send Donation
```typescript
server.tool("sendDonation", { amount: z.number() })
```
Sends a donation to the smart contract.

#### 2. View Top Donor
```typescript
server.tool("top_Donner_Donation", {})
```
Retrieves information about the top donor.

## 📁 Project Structure

```
mcp_server_EVM_contract/
├── index.ts           # Main MCP server implementation
├── package.json       # Project dependencies and scripts
├── tsconfig.json      # TypeScript configuration
├── .env.example       # Environment variable template
├── .gitignore        # Git ignore rules
└── README.md         # Project documentation
```

## 🔐 Security

⚠️ **Important Security Notes:**
- Never commit your `.env` file or expose your private keys
- Keep your `PRIVATE_KEY` secure and never share it
- Use a separate wallet for testing purposes
- Consider using hardware wallets for production deployments

## 📝 Scripts

- `npm run build`: Compile TypeScript to JavaScript
- `npm start`: Run the compiled server
- `npm test`: Run tests (not yet implemented)

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the issues page.

## 📄 License

ISC

## 👤 Author

**Tanzim Hossain Safin**
- GitHub: [@TanzimHossainSafin](https://github.com/TanzimHossainSafin)

## 🔗 Resources

- [Model Context Protocol Documentation](https://modelcontextprotocol.io/)
- [Ethers.js Documentation](https://docs.ethers.org/)
- [TypeScript Documentation](https://www.typescriptlang.org/docs/)

---

*This project is part of exploring Model Context Protocol integration with blockchain smart contracts.*
