## Guardian Chain

**Decentralized and Secure Digital Asset Recovery**

Guardian Chain is an innovative solution designed to protect your digital assets from loss due to forgotten keys, lost devices, or unforeseen situations. Leveraging the power of Smart Accounts, biometrics, and a network of trusted social guardians, Guardian Chain provides a robust, private, and user-friendly recovery mechanism.

---

### ✨ Key Features

* **Safe Smart Account with Internal Module**: Extends the functionality of existing secure accounts with our custom recovery logic, ensuring maximum fund security.

* **Privacy-Preserving Recovery (FHE-ready)**: Designed for future integrations with Zama’s Fully Homomorphic Encryption (FHE), enabling biometric verification without exposing sensitive data.

* **Verified Social Guardians via Farcaster**: Allows users to designate up to two trusted guardians, whose identity can be verified through their Farcaster handles and on-chain attestations.

* **Biometric Identity Verification (WebAuthn/Passkey)**: Uses biometrics (fingerprint, facial recognition) and passkeys for fast, secure access, with access attempt counters and biometric hash storage on IPFS/Filecoin.

* **Automated Timers and Notifications (Chainlink)**: Implements inactivity time-locks and scheduled notifications (e.g., “24 hours left before your time-lock expires”) using Chainlink Keepers and Functions.

* **Decentralized Storage (IPFS/Filecoin)**: Securely and redundantly stores biometric hashes and other critical recovery data.

* **Transparent Incentive Model**: A single 0.5% fee is automatically charged after the third recovery in a year, implemented as a “vault cost” that is either burned or redistributed.

* **Multilingual & Accessible UX**: Intuitive user interface in Spanish, English, and Portuguese, with Dark Mode, readable typography, and Mobile-First design, compliant with WCAG 2.1.

* **Tutorial & Practice Mode**: Guided onboarding and a practice mode so users can familiarize themselves with the recovery process risk-free.

---

### 🏗️ Project Architecture

Guardian Chain consists of two main modules:

1. **Smart Contracts (Solidity)**

   * **RecoveryModule**: An internal module for Safe Smart Accounts managing recovery logic, guardians, biometrics, and time-locks.
   * Integration with Chainlink for automation and notifications.
   * Prepared for guardian verification via Farcaster attestations.
   * Deployed on Base Sepolia (for the hackathon).

2. **Frontend (Next.js Mini App)**

   * Built with Next.js 14, Wagmi, and RainbowKit for smooth blockchain interaction.
   * Integration with the browser’s WebAuthn API for biometric management.
   * Decentralized storage management using IPFS/Filecoin libraries.
   * Designed as a Mini App optimized for the Base ecosystem.

---

### 🛠️ Tech Stack

* **Smart Contracts**: Solidity, Hardhat, OpenZeppelin, Safe Protocol Kit, Chainlink Contracts
* **Blockchain**: Base (Sepolia Testnet)
* **Frontend**: Next.js 14, React, TypeScript, Wagmi, Viem, RainbowKit, Tailwind CSS
* **Biometrics**: WebAuthn API
* **Decentralized Storage**: IPFS, Filecoin
* **Automation/Oracles**: Chainlink Keepers, Chainlink Functions
* **Social Identity**: Farcaster (conceptual/integration via attestations)
* **DevOps**: GitHub Actions (CI/CD), Jest (Testing), Docker (development environment)

---

### 🚀 Getting Started (For Developers)

To set up Guardian Chain in your local environment, follow these steps:

#### 1. Prerequisites

Make sure you have installed:

* Git
* Node.js (v18+) and npm
* Python (v3.9+) and pip
* Docker and Docker Compose
* Visual Studio Code (recommended)

#### 2. Clone the Repository

```bash
git clone [GUARDIAN_CHAIN_REPO_URL]
cd guardian-chain
```

#### 3. Environment Variables Setup

Copy the `.env.example` file and rename it to `.env` at the project root. Fill in the required variables:

```bash
cp .env.example .env
```

Edit `.env` with your private keys, Basescan API keys, and WalletConnect Project ID.

#### 4. Smart Contracts

```bash
cd contracts
npm install
npx hardhat compile
# Deploy to Base Sepolia (make sure you have test funds)
# npx hardhat run scripts/deploy.ts --network baseSepolia
# Run tests
npx hardhat test
```

#### 5. Frontend

```bash
cd app
npm install
npm run build   # Build the application
npm run dev     # Start the development server
# Run tests
npm test
```

Your frontend app will be available at [http://localhost:3000](http://localhost:3000).

---

### 🏆 Alignment with Aleph Hackathon

Guardian Chain is strongly aligned with several key tracks of the Aleph Hackathon:

* **Zama Track**: Future integration of FHE for biometric privacy.
* **Filecoin Track**: Use of IPFS/Filecoin for decentralized storage of critical data.
* **Base Track**: Development as a Mini App optimized for the Base ecosystem.
* **Lisk Founder Track**: Building a decentralized app solving a real-world problem with real-world impact.

---

### 🛣️ Next Steps (Post-Hackathon)

* Full FHE (Zama) implementation for private biometric verification.
* Robust integration with Farcaster and Ethereum Attestation Service (EAS).
* Advanced notification system (Push Protocol, SendGrid).
* Gas optimization and scalability improvements.
* Security audits and decentralized governance.

---

### 📄 License

This project is under the Apache 2.0 License. See the LICENSE file for details.
created by CynthiaOrtizOviedo
