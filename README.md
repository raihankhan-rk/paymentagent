# Payment Agent Chatbot with Memory

A DeFi payment agent chatbot built with XMTP for messaging and Mem0 for persistent memory. The agent helps users manage crypto payments while maintaining context of conversations.

## Demo Video

<a href="https://www.loom.com/share/fa927432f04b40ffba8754bc4f03d90b?sid=2b672665-706a-4bda-9ac0-40b8e72d2152" target="_blank">
</a>

*Click the image above to watch the demo video*


## Features

- **XMTP Messaging**: Secure, decentralized messaging protocol
- **Persistent Memory**: Remembers context from previous conversations using Mem0
- **DeFi Operations**: Handles crypto payments and wallet management
- **Base Sepolia Support**: Built for Base Sepolia testnet with USDC

## Prerequisites

- Node.js v18+
- npm or yarn
- OpenAI API key
- Mem0 API key
- CDP API credentials
- XMTP environment setup

## Setup

1. Clone the repository
2. Install dependencies:
```bash
yarn install
```

3. Create a `.env` file with the following variables:
```env
OPENAI_API_KEY=your_openai_api_key
MEM0_API_KEY=your_mem0_api_key
CDP_API_KEY_NAME=your_cdp_key_name
CDP_API_KEY_PRIVATE_KEY=your_cdp_private_key
WALLET_KEY=your_wallet_private_key
ENCRYPTION_KEY=your_encryption_key
XMTP_ENV=production  # or development
NETWORK_ID=base-sepolia  # optional, defaults to base-sepolia
```

4. Start the bot:
```bash
yarn dev
```

## Usage

1. Chat with the bot on xmtp.chat
2. Send messages to interact with the payment agent
3. The bot will remember context from previous conversations
4. Use natural language to request payments or check balances

## Memory Features

The bot uses Mem0 to maintain conversation context:
- Automatically stores all conversations
- Searches previous interactions for relevant context
- Provides more contextual responses based on conversation history

## Environment Variables

- `OPENAI_API_KEY`: Your OpenAI API key for the language model
- `MEM0_API_KEY`: Your Mem0 API key for persistent memory
- `CDP_API_KEY_NAME`: Coinbase Developer Platform API key name
- `CDP_API_KEY_PRIVATE_KEY`: Coinbase Developer Platform private key
- `WALLET_KEY`: Private key for the bot's wallet
- `ENCRYPTION_KEY`: XMTP encryption key
- `XMTP_ENV`: XMTP environment (production/development)
- `NETWORK_ID`: Network ID for transactions (defaults to base-sepolia)

## Storage

The bot uses local storage for:
- Wallet data: `.data/wallets/`
- XMTP data: `.data/xmtp/`

## License

MIT 