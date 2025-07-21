# 🤖 Mikrotik WhatsApp AI Bot

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://python.org)
[![RouterOS](https://img.shields.io/badge/RouterOS-7.x-red.svg)](https://mikrotik.com)
[![WhatsApp](https://img.shields.io/badge/WhatsApp-Bot-green.svg)](https://whatsapp.com)
[![Gemini AI](https://img.shields.io/badge/Gemini-2.0%20Flash-purple.svg)](https://ai.google.dev)

> Intelligent Mikrotik router monitoring and management through WhatsApp with AI-powered network analysis

## 🌟 Features

### 🔧 Router Management
- **Multi-user Support**: Each user manages their own routers
- **Easy Configuration**: Add routers via simple WhatsApp commands
- **Connection Testing**: Verify router connectivity before monitoring
- **Secure Authentication**: Individual router credentials per user

### 📊 Real-time Monitoring
- **System Information**: CPU, memory, uptime, and hardware details
- **Interface Traffic**: RX/TX rates with formatted bandwidth display
- **Network Status**: Netwatch monitoring for critical hosts
- **Hotspot Users**: Active WiFi users and session details
- **DHCP Leases**: IP assignments and device identification

### 🧠 AI-Powered Analysis
- **Traffic Analysis**: Gemini AI analyzes network patterns and bottlenecks
- **Security Assessment**: Automated security audit with threat detection
- **Health Check**: Router performance optimization recommendations
- **Natural Language**: Ask questions about your network in plain language

### 💰 Subscription System
- **Free Trial**: 3-hour trial for new users (1 router limit)
- **Flexible Plans**: Multiple subscription packages available
- **Auto-billing**: Integrated Midtrans payment processing
- **Instant Activation**: Automatic subscription activation post-payment

### 👨‍💼 Admin Features
- **Transaction Management**: View and manage all user transactions
- **Subscription Control**: Manual subscription management
- **User Analytics**: Monitor system usage and performance
- **Payment Tracking**: Real-time payment status monitoring

## 🚀 Quick Start

### Prerequisites
- Python 3.8+
- Mikrotik router with API access enabled
- WhatsApp Business account
- Google Gemini API key
- Midtrans merchant account

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/classyid/mikrotik-whatsapp-ai-bot.git
   cd mikrotik-whatsapp-ai-bot
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Configure environment**
   ```bash
   cp config.example.py config.py
   # Edit config.py with your API keys
   ```

4. **Run the bot**
   ```bash
   python main.py
   ```

### Configuration

```python
# Gemini AI Configuration
GEMINI_API_KEY = "your_gemini_api_key"
GEMINI_MODEL = "gemini-2.0-flash"

# Midtrans Configuration
MIDTRANS_API_URL = "your_midtrans_bridge_url"
MIDTRANS_API_KEY = "your_api_key"
MIDTRANS_APP_CODE = "your_app_code"

# Admin Configuration
ADMIN_NUMBERS = ["6281234567890"]  # WhatsApp numbers with admin access
```

## 📱 Usage

### Basic Commands

#### Router Management
```
mikrotik add [id] [host] [username] [password] [port] [name]
mikrotik list
mikrotik remove [id]
mikrotik test [id]
```

#### Monitoring Commands
```
mikrotik info [id]     # System information
mikrotik traffic [id]  # Interface traffic
mikrotik status [id]   # Complete status
mikrotik netwatch [id] # Network monitoring
mikrotik hotspot [id]  # Active WiFi users
mikrotik dhcp [id]     # DHCP leases
```

#### AI Assistant
```
mikrotik analyze [id]   # AI traffic analysis
mikrotik security [id]  # Security assessment
mikrotik health [id]    # Health recommendations
mikrotik ask [question] # Natural language queries
```

#### Subscription
```
langganan              # View available packages
langganan [package_id] # Subscribe to package
cek pembayaran         # Check payment status
```

### Example Usage

1. **Add your router:**
   ```
   mikrotik add home 192.168.1.1 admin mypassword 8728 Home Router
   ```

2. **Monitor traffic:**
   ```
   mikrotik traffic home
   ```

3. **AI analysis:**
   ```
   mikrotik ask home why is my internet slow?
   ```

4. **Subscribe:**
   ```
   langganan 1
   ```

## 🏗️ Architecture

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   WhatsApp      │    │   Python Bot    │    │   Mikrotik      │
│   Client        │◄──►│   (Neonize)     │◄──►│   Router        │
└─────────────────┘    └─────────────────┘    └─────────────────┘
                              │
                    ┌─────────┼─────────┐
                    │         │         │
            ┌───────▼───┐ ┌───▼───┐ ┌───▼────┐
            │ Gemini AI │ │SQLite │ │Midtrans│
            │  Analysis │ │  DB   │ │Payment │
            └───────────┘ └───────┘ └────────┘
```

## 📊 Subscription Packages

| Package | Routers | Duration | Price | Features |
|---------|---------|----------|-------|----------|
| Basic   | 1       | 30 days  | $5    | All monitoring |
| Pro     | 2       | 30 days  | $7    | Multi-router |
| Trial   | 1       | 14 days  | $3    | Testing |

## 🔒 Security

- **API Authentication**: Secure RouterOS API connections
- **User Isolation**: Each user's data is completely separated
- **Admin Controls**: Restricted admin commands
- **Payment Security**: PCI-compliant Midtrans integration
- **Data Protection**: Local JSON storage with proper access controls

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

- 📧 Email: kontak@classy.id
- 💬 WhatsApp: +62 812-4131-4446


## 🙏 Acknowledgments

- [Neonize](https://github.com/krypton-byte/neonize) - WhatsApp Web API
- [RouterOS API](https://help.mikrotik.com/docs/display/ROS/API) - Mikrotik integration
- [Google Gemini](https://ai.google.dev/) - AI analysis capabilities
- [Midtrans](https://midtrans.com/) - Payment processing

---

**Made with ❤️ for network administrators who love automation**
