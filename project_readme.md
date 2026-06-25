# StellarPay Student Wallet

StellarPay is a production-quality Stellar dApp designed specifically for students. It combines the speed of the Stellar network with the power of Soroban smart contracts to create a modern, rewarding payment ecosystem.

## 🚀 Features

- **Freighter Integration**: Seamless wallet connection and transaction signing.
- **XLM Payments**: Send instant, low-cost payments on the Stellar Testnet.
- **Soroban Rewards**: Earn points through a custom smart contract for academic milestones.
- **Live Monitoring**: Real-time event stream for contract activity.
- **Technical Explorer**: Direct interaction interface for Soroban contract functions.
- **Premium UI**: Glassmorphic dark theme with smooth Framer Motion transitions.

## 🛠 Tech Stack

- **Frontend**: React, Vite, TypeScript
- **Styling**: Tailwind CSS, Framer Motion
- **Blockchain**: Stellar SDK, Soroban SDK
- **Wallet**: Freighter Wallet
- **Network**: Stellar Testnet

## 📂 Project Structure

```text
src/
├── components/ # Shared UI (Nav, Cards, Modals)
├── pages/      # Route components (Dashboard, Send, Rewards)
├── layouts/    # Page wrappers and shells
├── services/   # Stellar & Soroban API logic
├── wallet/     # Freighter integration helpers
├── contracts/  # Smart contract ABIs and logic
├── hooks/      # Custom React hooks (useBalance, useEvents)
└── contexts/   # Global state (WalletContext, ThemeContext)
```

## 📋 Getting Started

1. **Environment Setup**:
   Create a `.env` file with `VITE_CONTRACT_ID` and `VITE_NETWORK=testnet`.
2. **Install Dependencies**: `npm install`
3. **Run Locally**: `npm run dev`

## 🔗 Contract Integration

The app is pre-configured to work with the following Soroban functions:
- `register_student(name: String)`
- `reward_student(wallet: Address, points: u32)`
- `get_student_points(wallet: Address)`
- `claim_reward(points: u32)`

---
Built on Stellar for the next generation of fintech.
