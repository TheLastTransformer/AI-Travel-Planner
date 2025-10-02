"# 🌍 AI Travel Planner

<div align="center">

![AI Travel Planner Logo](https://img.shields.io/badge/AI-Travel%20Planner-blue?style=for-the-badge&logo=airplane&logoColor=white)

[![GSSoC 2025](https://img.shields.io/badge/GSSoC-2025-orange?style=for-the-badge)](https://gssoc.girlscript.tech/)
[![Hacktoberfest 2025](https://img.shields.io/badge/Hacktoberfest-2025-purple?style=for-the-badge)](https://hacktoberfest.com/)
[![Open Source](https://img.shields.io/badge/Open%20Source-❤️-red?style=for-the-badge)](https://opensource.org/)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Streamlit](https://img.shields.io/badge/Streamlit-1.28+-red.svg)](https://streamlit.io/)
[![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)](CONTRIBUTING.md)

**An intelligent, AI-powered travel planning platform built with Streamlit and Large Language Models**

[🚀 Demo](#demo) • [📖 Documentation](#documentation) • [🤝 Contributing](#contributing) • [📞 Support](#support)

</div>

---

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Quick Start](#quick-start)
- [Installation](#installation)
- [Usage](#usage)
- [API Documentation](#api-documentation)
- [Contributing](#contributing)
- [GSSoC & Hacktoberfest](#gssoc--hacktoberfest)
- [Roadmap](#roadmap)
- [License](#license)
- [Support](#support)

## 🌟 Overview

AI Travel Planner is an innovative, open-source travel planning application that leverages the power of Artificial Intelligence to create personalized travel experiences. Built with Streamlit and powered by advanced Large Language Models, this platform helps travelers plan their perfect trip with intelligent recommendations, real-time bookings, and interactive assistance.

### 🎯 Mission
To democratize travel planning by providing an AI-powered, community-driven platform that makes travel accessible, affordable, and enjoyable for everyone.

## ✨ Features

### 🧠 AI-Powered Planning
- **Intelligent Itinerary Generation**: Create personalized travel plans based on preferences, budget, and interests
- **Smart Destination Recommendations**: Discover hidden gems and popular attractions tailored to your style
- **Dynamic Trip Optimization**: Real-time adjustments based on weather, events, and availability

### 🤖 Interactive Chatbot
- **24/7 Travel Assistant**: Get instant answers to travel-related questions
- **Multi-language Support**: Communicate in your preferred language
- **Context-Aware Responses**: Personalized advice based on your travel history and preferences

### 🔍 Smart Search & Discovery
- **Destination Explorer**: Comprehensive information about destinations worldwide
- **Activity Finder**: Discover activities, attractions, and experiences
- **Local Insights**: Get insider tips and cultural information

### 💰 Booking & Offers
- **Flight Search**: Find and compare flight options across multiple airlines
- **Hotel Booking**: Discover and book accommodations that fit your budget
- **Train Reservations**: Book train tickets with real-time availability
- **Deal Finder**: Automatic detection of discounts and special offers
- **Price Tracking**: Monitor price changes and get alerts for better deals

### 📊 Analytics & Insights
- **Travel Analytics**: Track your travel patterns and spending
- **Budget Management**: Smart budget allocation and expense tracking
- **Trip History**: Maintain a comprehensive record of your travels

## 🛠 Tech Stack

### Frontend
- **[Streamlit](https://streamlit.io/)** - Modern web framework for data applications
- **HTML/CSS/JavaScript** - Custom styling and interactions

### Backend & AI
- **[Python 3.8+](https://python.org/)** - Core programming language
- **Large Language Models (LLMs)** - AI-powered travel assistance
- **[OpenAI API](https://openai.com/api/)** / **[Hugging Face](https://huggingface.co/)** - Language model integration
- **[LangChain](https://langchain.com/)** - LLM application framework

### APIs & Services
- **Travel APIs** - Flight, hotel, and activity data
- **Weather APIs** - Real-time weather information
- **Maps APIs** - Location and navigation services
- **Payment Gateways** - Secure booking transactions

### Database & Storage
- **SQLite/PostgreSQL** - Data persistence
- **Redis** - Caching and session management

## 🚀 Quick Start

Get AI Travel Planner running on your local machine in just a few steps:

```bash
# Clone the repository
git clone https://github.com/TheLastTransformer/AI-Travel-Planner.git
cd AI-Travel-Planner

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Set up environment variables
cp .env.example .env
# Edit .env with your API keys

# Run the application
streamlit run app.py
```

Visit `http://localhost:8501` to start planning your next adventure! 🎉

## 📦 Installation

### Prerequisites
- Python 3.8 or higher
- pip package manager
- Git

### Detailed Setup

1. **Clone the Repository**
   ```bash
   git clone https://github.com/TheLastTransformer/AI-Travel-Planner.git
   cd AI-Travel-Planner
   ```

2. **Create Virtual Environment**
   ```bash
   python -m venv venv
   
   # Activate virtual environment
   # On Windows
   venv\Scripts\activate
   
   # On macOS/Linux
   source venv/bin/activate
   ```

3. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Environment Configuration**
   ```bash
   cp .env.example .env
   ```
   
   Edit `.env` file with your API keys:
   ```env
   OPENAI_API_KEY=your_openai_api_key
   TRAVEL_API_KEY=your_travel_api_key
   WEATHER_API_KEY=your_weather_api_key
   ```

5. **Database Setup**
   ```bash
   python setup_database.py
   ```

6. **Run the Application**
   ```bash
   streamlit run app.py
   ```

## 🎮 Usage

### Planning Your First Trip

1. **Start the Application**: Launch the Streamlit app
2. **Create Profile**: Set up your travel preferences
3. **Destination Input**: Enter your desired destination or let AI suggest
4. **Customize Preferences**: Select dates, budget, interests, and travel style
5. **Generate Itinerary**: Let AI create your personalized travel plan
6. **Book & Go**: Use integrated booking features for flights, hotels, and activities

### Using the Chatbot

- **Ask Questions**: "What's the best time to visit Japan?"
- **Get Recommendations**: "Suggest restaurants in Paris for under $50"
- **Plan Activities**: "Create a 3-day itinerary for Rome"
- **Check Weather**: "What's the weather like in Bali next week?"

## 📚 API Documentation

### Core Endpoints

```python
# Generate Travel Plan
POST /api/generate-plan
{
  "destination": "Paris, France",
  "duration": 5,
  "budget": 2000,
  "interests": ["culture", "food", "history"]
}

# Chat with AI Assistant
POST /api/chat
{
  "message": "What are the must-visit places in Tokyo?",
  "context": "planning_trip"
}

# Search Flights
GET /api/flights/search?from=NYC&to=PAR&date=2025-06-15

# Book Hotel
POST /api/hotels/book
{
  "hotel_id": "12345",
  "check_in": "2025-06-15",
  "check_out": "2025-06-20"
}
```

## 🤝 Contributing

We ❤️ contributions from the community! AI Travel Planner is built by developers, for developers.

### How to Contribute

1. **Fork the Repository**
   ```bash
   git clone https://github.com/YOUR_USERNAME/AI-Travel-Planner.git
   ```

2. **Create Feature Branch**
   ```bash
   git checkout -b feature/amazing-feature
   ```

3. **Make Changes**
   - Write clean, documented code
   - Follow our coding standards
   - Add tests for new features

4. **Commit Changes**
   ```bash
   git commit -m "Add amazing feature"
   ```

5. **Push to Branch**
   ```bash
   git push origin feature/amazing-feature
   ```

6. **Open Pull Request**
   - Describe your changes
   - Link any related issues
   - Request review from maintainers

### Contribution Guidelines

- **Code Style**: Follow PEP 8 for Python code
- **Documentation**: Update docs for any new features
- **Testing**: Write tests for new functionality
- **Issues**: Use issue templates for bug reports and feature requests

### Good First Issues

Look for issues labeled with:
- `good first issue` - Perfect for beginners
- `help wanted` - Community assistance needed
- `documentation` - Improve project docs
- `bug` - Fix existing issues

## 🏆 GSSoC & Hacktoberfest

### GSSoC 2025 Participants

Welcome to **GirlScript Summer of Code 2025**! 🎉

- **Mentorship**: Get guidance from experienced developers
- **Learning Path**: Structured learning with real-world projects
- **Community**: Join our Discord for collaboration
- **Recognition**: Certificates and swag for contributors

### Hacktoberfest 2025 Contributors

Celebrate **Hacktoberfest 2025** with us! 🎃

- **Quality PRs**: Focus on meaningful contributions
- **No Spam**: We review all PRs for quality
- **Learn & Grow**: Enhance your open-source skills
- **Prizes**: Eligible for Hacktoberfest rewards

### Special Labels
- `gssoc` - Issues suitable for GSSoC participants
- `hacktoberfest` - Issues eligible for Hacktoberfest
- `beginner-friendly` - Perfect for newcomers

## 🗺 Roadmap

### Q4 2025
- [ ] **Core Features**
  - [x] Basic AI travel planning
  - [ ] Multi-language chatbot
  - [ ] Flight booking integration
  - [ ] Hotel reservation system

### Q1 2026
- [ ] **Enhanced Features**
  - [ ] Train booking system
  - [ ] Advanced analytics dashboard
  - [ ] Mobile app development
  - [ ] Offline mode support

### Q2 2026
- [ ] **Platform Expansion**
  - [ ] Third-party integrations
  - [ ] Enterprise features
  - [ ] API marketplace
  - [ ] Community marketplace

### Future Vision
- AI-powered travel predictions
- VR/AR trip previews
- Blockchain-based travel rewards
- IoT integration for smart travel

## 🏗 Project Structure

```
AI-Travel-Planner/
├── 📁 src/
│   ├── 📁 components/        # Reusable UI components
│   ├── 📁 pages/            # Streamlit pages
│   ├── 📁 ai/               # AI/ML modules
│   ├── 📁 api/              # API integrations
│   └── 📁 utils/            # Utility functions
├── 📁 tests/                # Test suite
├── 📁 docs/                 # Documentation
├── 📁 data/                 # Sample data and models
├── 📁 scripts/              # Automation scripts
├── 📄 app.py                # Main Streamlit application
├── 📄 requirements.txt      # Python dependencies
├── 📄 .env.example          # Environment variables template
└── 📄 README.md             # This file
```

## 🔧 Development Setup

### Environment Setup
```bash
# Install development dependencies
pip install -r requirements-dev.txt

# Pre-commit hooks
pre-commit install

# Run tests
pytest

# Code formatting
black .
isort .

# Linting
flake8 .
```

### Docker Setup
```bash
# Build image
docker build -t ai-travel-planner .

# Run container
docker run -p 8501:8501 ai-travel-planner
```

## 📊 Statistics

<div align="center">

![GitHub stars](https://img.shields.io/github/stars/TheLastTransformer/AI-Travel-Planner?style=social)
![GitHub forks](https://img.shields.io/github/forks/TheLastTransformer/AI-Travel-Planner?style=social)
![GitHub issues](https://img.shields.io/github/issues/TheLastTransformer/AI-Travel-Planner)
![GitHub pull requests](https://img.shields.io/github/issues-pr/TheLastTransformer/AI-Travel-Planner)

</div>

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2025 AI Travel Planner Contributors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.
```

## 🤝 Support

### Community Support
- **Discord**: [Join our community](https://discord.gg/ai-travel-planner)
- **GitHub Discussions**: [Ask questions and share ideas](https://github.com/TheLastTransformer/AI-Travel-Planner/discussions)
- **Stack Overflow**: Tag your questions with `ai-travel-planner`

### Maintainers
- **@TheLastTransformer** - Project Lead & Maintainer
- **@Contributors** - Community Contributors

### Getting Help
1. **Check Documentation**: Search our docs first
2. **Browse Issues**: Your question might already be answered
3. **Create Issue**: Use our issue templates
4. **Join Community**: Connect with other developers

---

<div align="center">

### 🌟 Star History

[![Star History Chart](https://api.star-history.com/svg?repos=TheLastTransformer/AI-Travel-Planner&type=Date)](https://star-history.com/#TheLastTransformer/AI-Travel-Planner&Date)

### 🙏 Acknowledgments

Thanks to all the amazing contributors who make this project possible!

[![Contributors](https://contrib.rocks/image?repo=TheLastTransformer/AI-Travel-Planner)](https://github.com/TheLastTransformer/AI-Travel-Planner/graphs/contributors)

---

**Made with ❤️ by the AI Travel Planner Community**

[⬆ Back to Top](#-ai-travel-planner)

</div>" 
