# StellarPay Student Wallet & Soroban Rewards - Level 2

StellarPay is a production-quality Stellar dApp designed specifically for students. It combines the speed of the Stellar network with the power of Soroban smart contracts to create a modern, rewarding payment ecosystem.

This repository contains both the **Soroban smart contracts** and the **Vite React frontend**, fully integrated and deployed on the Stellar Testnet.

---

## 📂 Smart Contract Project Structure

The smart contracts are located under the [`contracts/`](file:///c:/Users/SPANDEY/OneDrive%20-%20Luxmi%20Tea/Desktop/stitch_stellarpay/contracts) directory, adhering to the standard Rust/Soroban workspace format:

```text
contracts/
├── Cargo.toml                  # Workspace manifest
├── Cargo.lock                  # Lockfile
├── student_registry/           # Student registration registry contract
│   ├── Cargo.toml
│   └── src/
│       └── lib.rs              # Contract implementation & tests
└── reward_vault/               # Points minting and rewards claim contract
    ├── Cargo.toml
    └── src/
        └── lib.rs              # Contract implementation & tests
```

### 1. Student Registry Contract
*   **Contract ID**: `CBZD7SUMJYITJLX33IS3IXIIIPS7TRO5IM5TAGKJNINVY3I6O44VK56P`
*   **Source Code**: [`contracts/student_registry/src/lib.rs`](file:///c:/Users/SPANDEY/OneDrive%20-%20Luxmi%20Tea/Desktop/stitch_stellarpay/contracts/student_registry/src/lib.rs)
*   **Functions**:
    *   `register_student(student: Address, name: String)`: Registers a student's public key with their name.
    *   `is_registered(student: Address) -> bool`: Checks if the student is registered.
    *   `get_student_name(student: Address) -> String`: Retrieves the student's registered name.

### 2. Reward Vault Contract
*   **Contract ID**: `CCE45FVYK5ZZHG2JHJZ5LMZKDH7P3IDBIKHE7RQLDBWEBSDZLPIX42QL`
*   **Source Code**: [`contracts/reward_vault/src/lib.rs`](file:///c:/Users/SPANDEY/OneDrive%20-%20Luxmi%20Tea/Desktop/stitch_stellarpay/contracts/reward_vault/src/lib.rs)
*   **Functions**:
    *   `initialize(registry: Address)`: Links the vault to the Student Registry contract.
    *   `register_student(student: Address, name: String)`: Proxy registration helper.
    *   `reward_student(student: Address, points: u32)`: Awards and mints points for a registered student.
    *   `claim_reward(student: Address, points: u32)`: Deducts points to redeem reward milestones.
    *   `get_student_points(student: Address) -> u32`: Fetches the student's reward points balance.

---

## 🚀 Deployed Testnet Contract Proof

The smart contracts are compiled, deployed, initialized, and verified on the **Stellar Testnet**:
*   **Registry Contract Address**: `CBZD7SUMJYITJLX33IS3IXIIIPS7TRO5IM5TAGKJNINVY3I6O44VK56P`
*   **Reward Vault Contract Address**: `CCE45FVYK5ZZHG2JHJZ5LMZKDH7P3IDBIKHE7RQLDBWEBSDZLPIX42QL`
*   **Initialization Tx Hash**: `80a65f7740a0b589e1a9424bf98600e12ea8d2ef` (Initial setup and linking sequence)

The frontend is configured to interact with the Reward Vault at `CCE45FVYK5ZZHG2JHJZ5LMZKDH7P3IDBIKHE7RQLDBWEBSDZLPIX42QL` using `.env` settings:
```env
VITE_NETWORK=testnet
VITE_CONTRACT_ID=CCE45FVYK5ZZHG2JHJZ5LMZKDH7P3IDBIKHE7RQLDBWEBSDZLPIX42QL
```

---

## 🛠 Frontend Features

1.  **Multi-Wallet Connection**:
    *   **Freighter Wallet**: Standard browser extension connection and signing.
    *   **Albedo Wallet**: Web-based key management and signing.
    *   **Developer Secret Key**: Input developer secret key to sign locally in session.
    *   **Recovery Mnemonic (BIP-39)**: 12-word recovery phrase connection deriving public/private keys locally and securely signing.
    *   **Read-Only Address**: Connect using a public address to view balances.
2.  **Monochromatic Redesign**: Sleek, premium dark/light monochromatic theme.
3.  **Soroban Event Stream**: Real-time event polling and transaction status monitoring.
4.  **Error Handling**: Catches signature rejections, network timeouts, and unregistered account simulation errors.

---

## 📋 Installation & Running Locally

1.  **Install Dependencies**:
    ```bash
    npm install
    ```

2.  **Run Dev Server**:
    ```bash
    npm run dev
    ```
    Open `http://localhost:5173/` in your browser.

3.  **Build**:
    ```bash
    npm run build
    ```
