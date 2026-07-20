cat > README.md << 'EOF'
# 🚀 MyZubster

**Decentralized Freelance Marketplace · Powered by Monero (XMR)**

MyZubster is an open-source, privacy-first platform that connects freelancers and clients directly. No middlemen, no censorship, no data harvesting.

---

## 🌐 Access MyZubster

| Method | URL |
|--------|-----|
| **Clearnet (IP)** | `http://188.213.161.186:4000` |
| **Tor (Onion)** | `http://olqcnbdlt35k2stmmwvzhvuetu2fc4us2jnn5wg6y6wlcddihfmdomid.onion` |
| **Domain** | `https://myzubster.com` *(coming soon)* |

---

## ✨ Features

- ✅ **Decentralized & Open Source** – No single point of failure
- ✅ **Monero (XMR) Payments** – Private, untraceable, borderless
- ✅ **NFT Marketplace** – Tokenized skills on Tari
- ✅ **AI Assistant** – Generate professional skill descriptions with Groq
- ✅ **JWT Authentication** – Secure user management
- ✅ **Escrow System** – Funds locked until service delivery
- ✅ **Tor Integration** – Anonymous access via Onion service
- ✅ **Privacy First** – No tracking, no data selling

---

## 🖼️ Screenshots

### NFT Marketplace

![NFT Marketplace](https://raw.githubusercontent.com/DanielIoni-creator/myzubster-assets/main/screenshot-nft-marketplace.png)

---

## 🧩 Architecture

MyZubster is built as a modular ecosystem:

| Component | Description | Status |
|-----------|-------------|--------|
| **Gateway** | Monero payment engine | ✅ Live |
| **Marketplace** | Backend API + UI | ✅ Live |
| **Mobile App** | React Native | 🚧 In Development |

### Tech Stack

- **Backend**: Node.js + Express
- **Database**: MongoDB (Gateway) + SQLite (Marketplace)
- **Authentication**: JWT
- **AI**: Groq API
- **Deployment**: Aruba Cloud VPS (Ubuntu 24.04)
- **Tor**: Onion Service for anonymous access

---

## 🛠️ Quick Start

### Prerequisites

- Node.js v18+
- npm v9+
- Docker (optional)

### Clone and Install

```bash
# Clone the repository
git clone https://github.com/DanielIoni-creator/MyZubster-Marketplace.git
cd MyZubster-Marketplace

# Install dependencies
npm install

# Configure environment
cp .env.example .env
nano .env

# Start the server
node server.js
