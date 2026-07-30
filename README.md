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
| [Telegram Bot & Channel](#-telegram-bot--channel) | Real‑time updates and community |
| [Arduino Garden API](#-arduino-garden-api) | IoT sensor integration |
| [Seed Exchange](#-seed-exchange) | Share seeds and cuttings |
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
Telegram Bot	Real‑time commit notifications and weekly stats	✅ Live
Arduino Garden API	IoT sensor data ingestion	✅ Live
Seed Exchange	P2P seed and cutting sharing	🚧 In Development
Tech Stack

    Backend: Node.js + Express

    Databases: MongoDB (Gateway) + SQLite (Marketplace)

    Authentication: JWT

    Payments: Monero (XMR)

    AI: DeepSeek / Groq API

    Deployment: Aruba Cloud VPS (Ubuntu 24.04)

    Privacy: Tor Onion Service

🤖 Telegram Bot & Channel

MyZubster has a public Telegram channel and an automated bot that keeps the community updated in real time.
Channel: @myzubster

    Receive notifications for every commit on the main repositories.

    Get weekly project statistics (transactions, XMR volume, active users).

    Stay informed about new bounties and milestones.

Bot: @MyZubster_bot

    Sends automatic notifications for push events via GitHub webhooks.

    Runs on a self‑hosted Node.js server with PM2.

    Supports payloads up to 100MB (handles large repositories).

    Also sends a weekly statistical report every Monday at 9:00 CET.

How to set up your own bot

    Create a Telegram bot via @BotFather.

    Clone the telegram-notifier repository (available on request).

    Configure the bot token and chat ID.

    Deploy with PM2.

📡 Arduino Garden API

The Arduino Garden API allows you to connect your smart garden to MyZubster.
It is designed for ESP8266/ESP32 boards with sensors for pH, EC, temperature, and humidity.
Endpoints
Method	Endpoint	Description
POST	/api/garden/data	Send sensor data (gardenId, ph, ec, temperature, humidity)
GET	/api/garden/:id/stats	Retrieve min, max, avg statistics for a garden
Example Payload (POST)
json

{
  "gardenId": "my-urban-garden",
  "ph": 6.2,
  "ec": 1.8,
  "temperature": 22.5,
  "humidity": 65
}

Example Response
json

{
  "success": true,
  "message": "Dati dell'orto salvati con successo",
  "data": {
    "gardenId": "my-urban-garden",
    "ph": 6.2,
    "ec": 1.8,
    "temperature": 22.5,
    "humidity": 65,
    "timestamp": "2026-07-30T12:00:45.996Z"
  }
}

Arduino Code (ESP8266)
cpp

#include <ESP8266WiFi.h>
#include <ArduinoJson.h>

const char* ssid = "your_wifi";
const char* password = "your_password";
const char* serverUrl = "http://188.213.161.186:3002/api/garden/data";

void setup() {
  Serial.begin(115200);
  WiFi.begin(ssid, password);
  while (WiFi.status() != WL_CONNECTED) delay(500);
  Serial.println("WiFi connected!");
}

void loop() {
  float ph = 6.2;
  float ec = 1.8;
  float temp = 22.5;
  float hum = 65;

  StaticJsonDocument<200> doc;
  doc["gardenId"] = "test-garden-001";
  doc["ph"] = ph;
  doc["ec"] = ec;
  doc["temperature"] = temp;
  doc["humidity"] = hum;

  String payload;
  serializeJson(doc, payload);

  WiFiClient client;
  if (client.connect("188.213.161.186", 3002)) {
    client.println("POST /api/garden/data HTTP/1.1");
    client.println("Host: 188.213.161.186:3002");
    client.println("Content-Type: application/json");
    client.print("Content-Length: ");
    client.println(payload.length());
    client.println();
    client.println(payload);
    delay(1000);
  }
  delay(60000); // Send every minute
}

🌱 Seed Exchange

MyZubster is building a decentralized seed and cutting exchange to promote biodiversity and local food production.
Features (coming soon)

    Users can list seeds, cuttings, seedlings, and bulbs.

    Exchange types: free, barter, donation.

    Geolocation support for local exchanges.

    Messaging system to coordinate trades.

    Integration with the global plant map.

Open Issues

We have 6 open issues for the Seed Exchange feature. Some are bounties (paid in XMR).
#	Repository	Type	Title	Bounty
1	MyZubster-Marketplace	Free	Data model for Seed Exchange	–
2	MyZubsterGateway	Bounty	API for Seed Exchange	0.06 XMR
3	MyZubsterWeb	Free	Frontend for listings	–
4	MyZubsterWeb	Free	Form to create listing	–
5	MyZubsterGateway	Bounty	Messaging for exchanges	0.05 XMR
6	myzubster	Free	Display on map	–

🔗 View all Seed Exchange issues
📡 API Reference

The main API endpoints are provided by the Gateway service:
Endpoint	Method	Description
/health	GET	Health check
/api/payments	POST	Create a payment
/api/payments/:id	GET	Check payment status
/api/webhook	POST	Webhook for order events
/api/users	GET	List users (admin)
/api/garden/data	POST	Send Arduino sensor data
/api/garden/:id/stats	GET	Garden statistics
/api/seed-exchange	GET/POST	Seed exchange listings

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

