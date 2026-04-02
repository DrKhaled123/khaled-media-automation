# 🤖 Khaled Media Automation

**Advanced Social Media Marketing Automation System**

[![Version](https://img.shields.io/badge/version-3.0-blue.svg)](https://github.com/DrKhaled123/khaled-media-automation)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

> Complete autonomous social media marketing system with anti-detection, self-healing, and session-based authentication.

## ✨ Features

- 🎯 **Multi-Platform Publishing** — Instagram, TikTok, Twitter/X, Facebook, LinkedIn, YouTube
- 🔒 **Session-Based Auth** — Username/password login with automatic cookie management
- 🕵️ **Anti-Block Strategies** — Fingerprint rotation, human behavior simulation, stealth mode
- 🩹 **Self-Healing** — Auto-fixes errors (rate limits, auth expiry, network issues)
- ⚡ **Parallel Processing** — Async multi-platform publishing
- 🤖 **AI-Powered Content** — Auto-generates SEO-optimized captions
- 📊 **Analytics & Reporting** — Performance tracking and insights

## 🚀 Quick Start

### Installation

```bash
# Clone the repository
git clone https://github.com/DrKhaled123/khaled-media-automation.git
cd khaled-media-automation

# Install dependencies
pip install -r requirements.txt

# Install Playwright browsers
playwright install chromium

# Configure environment
cp .env.example .env
# Edit .env with your credentials
```

### Usage

```python
from agent.social_agent import ContentBrief
from agent.orchestrator import SocialMediaOrchestrator

# Create content brief
brief = ContentBrief(
    content_file="./my_video.mp4",
    content_type="video",
    topic="Ramadan Health Tips",
    target_audience="Arabic adults 25-45",
    tone="educational",
    goal="engagement",
    platforms=["instagram", "tiktok", "twitter"]
)

# Execute publishing
orchestrator = SocialMediaOrchestrator()
results = await orchestrator.run(brief)
```

## 🔐 Session-Based Authentication

No API keys needed! Just provide username/password:

```bash
# Instagram
INSTAGRAM_USERNAME=your_username
INSTAGRAM_PASSWORD=your_password

# TikTok
TIKTOK_USERNAME=your_username
TIKTOK_PASSWORD=your_password

# Twitter
TWITTER_USERNAME=your_username
TWITTER_PASSWORD=your_password
```

The agent automatically:
1. Logs in via browser automation
2. Extracts and encrypts cookies
3. Reuses cookies for future sessions
4. Refreshes when expired

## 🛡️ Anti-Detection Features

| Technique | Description |
|-----------|-------------|
| **Fingerprint Rotation** | Unique browser signature per session |
| **Human Behavior** | Realistic typing, mouse movements, delays |
| **Request Randomization** | Varied headers, TLS fingerprints |
| **Timing Strategies** | Log-normal delays, human posting schedules |
| **Stealth Mode** | Playwright anti-detection patches |

## 📁 Project Structure

```
agent/
├── social_agent.py          # Core agent logic
├── orchestrator.py          # Publishing orchestration
├── session_manager.py       # Cookie management
├── self_healing/            # Error recovery
├── stealth/                 # Anti-detection
│   ├── fingerprints.py
│   ├── human_behavior.py
│   └── request_signatures.py
├── publishers/              # Platform publishers
│   ├── session_instagram.py
│   ├── session_tiktok.py
│   └── ...
└── hacks/                   # Platform-specific tricks
    ├── instagram_gql.py
    └── tiktok_sig.py
```

## 📝 Documentation

- **[SKILL.md](SKILL.md)** — Complete technical documentation
- **[AGENTS.md](AGENTS.md)** — Quick reference for AI agents

## ⚙️ Configuration

### Environment Variables

```bash
# Session Configuration
SESSION_STORAGE_PATH=~/.social_agent/sessions
SESSION_ENCRYPTION_KEY=your_random_32_char_key
SESSION_MAX_AGE_DAYS=7
SESSION_HEADLESS=true

# Circuit Breaker
CIRCUIT_FAILURE_THRESHOLD=5
CIRCUIT_RECOVERY_TIMEOUT=300
MAX_RETRIES=3

# AI Configuration
ANTHROPIC_API_KEY=your_key
```

## 🔧 Commands

| Command | Action |
|---------|--------|
| `publish` | Publish content immediately |
| `schedule` | Schedule for future time |
| `analyze` | Generate performance report |
| `fix` | Apply self-healing to errors |
| `status` | Check system health |

## 🛠️ Troubleshooting

| Issue | Solution |
|-------|----------|
| "Session expired" | Clear cookies: `rm ~/.social_agent/sessions/*` |
| "Rate limited" | Wait 15min, reduce frequency |
| "Captcha detected" | Set `SESSION_HEADLESS=false`, solve manually |
| "Element not found" | Update selectors in publisher code |

## 📊 Performance

- **Publishing Speed**: ~90 seconds for 5 platforms (parallel)
- **Memory Usage**: ~350MB stable
- **Success Rate**: >95% with self-healing

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## 📄 License

MIT License — see [LICENSE](LICENSE) file.

## 🙏 Acknowledgments

- Built with [Playwright](https://playwright.dev/)
- AI powered by [Anthropic Claude](https://anthropic.com/)
- Browser stealth by [playwright-stealth](https://github.com/AtuboDad/playwright-stealth)

---

**Made with 💫 by Khaled**