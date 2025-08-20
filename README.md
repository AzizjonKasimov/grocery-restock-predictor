# 🛒 Smart Grocery Restock Bot

A Telegram bot that intelligently predicts when you need to restock your groceries using machine learning and contextual data like weather patterns and user behavior.

## 🌟 Features

- **Zero Setup**: Just tell the bot what groceries you usually buy
- **Smart Predictions**: Uses machine learning to learn your consumption patterns
- **Context-Aware**: Considers weather, seasonality, and local events
- **Feedback-Driven**: Improves recommendations based on your approval/rejection
- **Privacy-First**: No need to input quantities or detailed purchase data

## 🚀 How It Works

1. **Setup**: Tell the bot your usual grocery items (e.g., "milk", "bread", "bananas")
2. **Learning**: The bot starts with conservative estimates and learns from your feedback
3. **Smart Notifications**: Get timely restock reminders based on:
   - Your historical patterns
   - Weather forecasts (affects fresh produce consumption)
   - Seasonal trends
   - Day of the week patterns
4. **Feedback Loop**: Simply approve ✅ or reject ❌ notifications to improve accuracy

## 🏗️ Architecture

- **Backend**: Python with `python-telegram-bot`
- **Database**: PostgreSQL for user data, Redis for caching
- **ML Approach**: Multi-Armed Bandit with contextual features
- **APIs**: OpenWeatherMap for weather data
- **Hosting**: Railway/Render/Google Cloud Run ready

## 🧠 Machine Learning Approach

The bot uses a **contextual multi-armed bandit** approach where:
- Each grocery item has multiple timing strategies
- Context includes weather, seasonality, user patterns, and feedback history
- Reward system: +1 for approved notifications, penalties for poor timing
- Gradual learning with conservative initial estimates

## 🔧 Installation

### Prerequisites
- Python 3.9+
- PostgreSQL
- Redis (optional, for caching)
- Telegram Bot Token

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/smart-grocery-restock-bot.git
   cd smart-grocery-restock-bot
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Environment Configuration**
   ```bash
   cp .env.example .env
   # Edit .env with your configuration
   ```

4. **Database Setup**
   ```bash
   python scripts/init_db.py
   ```

5. **Run the bot**
   ```bash
   python bot.py
   ```

## 📊 Configuration

Create a `.env` file with:

```env
TELEGRAM_BOT_TOKEN=your_telegram_bot_token
DATABASE_URL=postgresql://username:password@localhost/grocery_bot
OPENWEATHER_API_KEY=your_openweather_api_key
REDIS_URL=redis://localhost:6379 (optional)
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📈 Roadmap

- [ ] Basic grocery tracking and notifications
- [ ] Weather integration
- [ ] Multi-Armed Bandit implementation
- [ ] User feedback system
- [ ] Advanced ML features (seasonal patterns, local events)
- [ ] Analytics dashboard
- [ ] Multi-language support

## 🔒 Privacy

This bot is designed with privacy in mind:
- No detailed purchase tracking
- Only aggregated consumption patterns stored
- Optional data deletion
- Local deployment supported

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Built for users who want smarter grocery management
- Inspired by the need for intelligent, context-aware notifications
- Special thanks to the open-source community

## 📧 Contact

For questions or suggestions, please open an issue or contact [your-email@example.com].

---

⭐ If you find this project useful, please consider giving it a star!
