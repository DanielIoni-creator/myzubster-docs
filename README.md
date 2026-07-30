# 📚 MyZubster Documentation

**Welcome to the official documentation hub for the MyZubster ecosystem.**

---

## 🌐 About This Repository

This repository contains all the documentation for the MyZubster project.  
It serves as the central knowledge base for developers, users, and contributors.

**Key contents:**
- Project overview and architecture
- Setup and installation guides
- API references
- Contribution guidelines
- Economic and legal documentation

---

## 🧭 Quick Navigation

| Section | Description |
|---------|-------------|
| [Getting Started](#-getting-started) | How to set up and run MyZubster |
| [Architecture](#-architecture) | High‑level system design |
| [API Reference](#-api-reference) | Endpoints and usage |
| [Contributing](#-contributing) | How to help the project |
| [License](#-license) | MIT License |

---

## 🚀 Getting Started

### Prerequisites
- Node.js v18+
- npm v9+
- Docker (optional)

### Clone and Install

```bash
# Clone the marketplace (or any other component)
git clone https://github.com/MyZubster-Ecosystem/MyZubster-Marketplace.git
cd MyZubster-Marketplace

# Install dependencies
npm install

# Configure environment
cp .env.example .env
nano .env

# Start the server
node server.js
For detailed setup instructions, refer to the individual repository READMEs.
🧱 Architecture

MyZubster is built as a modular ecosystem:
Component	Description	Status
Gateway	Monero payment engine, webhooks, monitoring	✅ Live
Marketplace	Backend API + UI for services and skills	✅ Live
Mobile App	React Native client for Android	🚧 In Development
Web App	React/Vite frontend	✅ Live
Tech Stack

    Backend: Node.js + Express

    Databases: MongoDB (Gateway) + SQLite (Marketplace)

    Authentication: JWT

    Payments: Monero (XMR)

    AI: DeepSeek / Groq API

    Deployment: Aruba Cloud VPS (Ubuntu 24.04)

    Privacy: Tor Onion Service

📡 API Reference

The main API endpoints are provided by the Gateway service:
Endpoint	Method	Description
/health	GET	Health check
/api/payments	POST	Create a payment
/api/payments/:id	GET	Check payment status
/api/webhook	POST	Webhook for order events
/api/users	GET	List users (admin)

For full API documentation, see the Gateway repository.
🤝 Contributing

Contributions are welcome! Check out the open issues and the roadmap:

    Issues: https://github.com/MyZubster-Ecosystem/MyZubsterGateway/issues

    Roadmap: https://github.com/users/DanielIoni-creator/projects/1

How to Contribute

    Fork the repository you want to work on.

    Create a new branch for your feature or fix.

    Submit a pull request with a clear description of your changes.

For more details, see the CONTRIBUTING.md file in each repository.
📜 License

All MyZubster components are released under the MIT License – free for everyone to use, modify, and distribute.
🌐 Ecosystem Hub

MyZubster Ecosystem: https://github.com/MyZubster-Ecosystem

Maintained by Daniel Ioni and the MyZubster community.


## 💬 Community

- **Telegram**: [@MyZubster_bot](https://t.me/MyZubster_bot) – for updates, support, and discussions.


## 🌐 Connect with Us

- **Telegram**: [@MyZubster_bot](https://t.me/MyZubster_bot) – updates, support, and discussions
- **Twitter / X**: [@DanielIoni](https://twitter.com/DanielIoni) – project announcements and thoughts
- **TikTok**: [@danielioni](https://tiktok.com/@danielioni) – behind the scenes and project updates
- **Instagram**: [@danielioni](https://instagram.com/danielioni) – visuals and community stories
- **dev.to**: [Daniel Ioni](https://dev.to/danielioni) – technical articles and project updates
