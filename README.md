# BLOCN Exchange API Documentation

<p align="center">
  <img src="https://github.com/user-attachments/assets/92907e60-c0a9-4e44-b651-b489cb660257" alt="BLOCN Exchange API" width="200"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/version-v1.0.0-blue.svg" alt="Version">
  <img src="https://img.shields.io/badge/build-passing-brightgreen.svg" alt="Build Status">
  <img src="https://img.shields.io/badge/docs-latest-brightgreen.svg" alt="Documentation">
</p>

## 📚 Introduction

Welcome to BLOCN Exchange's official API documentation. This repository contains comprehensive documentation for integrating with BLOCN's trading platform, including RESTful APIs, WebSocket feeds, and example implementations.

## 🚀 Quick Start

### API Base URLs

plaintext
REST API: https://api.blocn1.com
WebSocket: wss://ws.blocn1.com


### Authentication

All private endpoints require API key authentication. To obtain your API keys:

1. Register at [BLOCN Exchange](https://www.blocn1.com)
2. Complete KYC verification
3. Generate API keys in your account settings

## 📋 API Documentation

### REST API

- [Authentication](/docs/rest-api/authentication.md)
- [Market Data](/docs/rest-api/market-data.md)
- [Spot Trading](/docs/rest-api/spot-trading.md)
- [Futures Trading](/docs/rest-api/futures-trading.md)
- [Account & Wallet](/docs/rest-api/account.md)

### WebSocket API

- [Connection Guide](/docs/websocket/connection.md)
- [Market Streams](/docs/websocket/market-streams.md)
- [Trading Streams](/docs/websocket/trading-streams.md)
- [Account Updates](/docs/websocket/account-updates.md)

## 💻 Code Examples

### REST API Examples

python
import requests

# Get market ticker
response = requests.get('https://api.blocn1.com/v1/ticker/BTC-USDT')
print(response.json())


### WebSocket Example

javascript
const ws = new WebSocket('wss://ws.blocn1.com');

ws.onopen = () => {
    ws.send(JSON.stringify({
        "method": "SUBSCRIBE",
        "params": ["btcusdt@ticker"],
        "id": 1
    }));
};

ws.onmessage = (event) => {
    console.log(event.data);
};


## 🔧 API Features

- REST API and WebSocket support
- Real-time market data
- Advanced order types
- Portfolio management
- Historical data access
- Rate limiting information
- Error handling guidelines

## 📈 Rate Limits

| Endpoint Type | Rate Limit |
|--------------|------------|
| Public REST  | 100 requests/minute |
| Private REST | 300 requests/minute |
| WebSocket    | Unlimited subscriptions |

## 🔐 Security

- HMAC SHA256 Authentication
- API Key & Secret Management
- IP Whitelisting
- Optional 2FA for API Operations

## 📖 Additional Resources

- [Error Codes Reference](/docs/error-codes.md)
- [Best Practices Guide](/docs/best-practices.md)
- [Trading Rules](/docs/trading-rules.md)
- [Change Log](/CHANGELOG.md)

## 💬 Support

- Technical Issues: api-support@blocn1.com
- Documentation Feedback: docs@blocn1.com
- Join our [Developer Discord](https://discord.gg/blocn-dev)

## 🤝 Contributing

We welcome contributions to our documentation! Please see our [Contributing Guidelines](CONTRIBUTING.md) for details.

## 📜 License

This documentation is licensed under [MIT License](LICENSE)

---

<p align="center">
  <b>Need help? Join our Developer Community</b>
</p>

<p align="center">
  <a href="https://www.blocn1.com">Website</a> •
  <a href="https://www.youtube.com/@Blocn_Official">Youtube</a> •
  <a href="https://x.com/blocn_global">Twitter</a> •
  <a href="https://blocn.medium.com/">Medium</a> •
  <a href="https://www.instagram.com/blocn_global/">Instagram</a>
</p>

<p align="center">
  © 2024 BLOCN Exchange. All Rights Reserved.
</p>
