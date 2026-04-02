# Social Media Marketing Automation Skill

**ID:** `social-media-marketing-automation`  
**Version:** 3.0  
**Author:** AI Assistant  
**Category:** Marketing / Automation

## Description

Complete autonomous social media marketing system with:
- Advanced anti-block strategies and stealth techniques
- Self-healing error recovery
- Session-based authentication (username/password)
- Multi-platform publishing (Instagram, TikTok, Twitter, Facebook, LinkedIn, YouTube)
- AI-powered content generation
- Performance optimization

## When to Use

Use this skill when:
- User wants to publish content to social media platforms
- User needs content scheduling automation
- User wants session-based auth (no official API keys needed)
- User needs anti-detection strategies for automation
- User wants self-healing automation that fixes its own errors

## Key Features

| Feature | Description |
|---------|-------------|
| Fingerprint Rotation | Unique browser fingerprint per session |
| Human Behavior Simulation | Realistic typing, mouse movements, delays |
| Self-Healing | Auto-fixes rate limits, auth expiry, network errors |
| Session Management | Automatic cookie extraction and reuse |
| Circuit Breakers | Prevents cascading failures |
| Async Publishing | Parallel multi-platform publishing |

## Commands

- `"Publish [content] to [platforms]"` - Publish content immediately
- `"Schedule [content] for [time]"` - Schedule future post
- `"Analyze performance"` - Generate analytics report
- `"Fix [issue]"` - Apply self-healing to errors
- `"Show status"` - Check system health

## Quick Start

```python
# Load skill and execute
from social_media_agent import ContentBrief
from orchestrator import SocialMediaOrchestrator

brief = ContentBrief(
    content_file="./video.mp4",
    topic="My Content",
    platforms=["instagram", "tiktok"]
)

orchestrator = SocialMediaOrchestrator()
results = await orchestrator.run(brief)
```

## Requirements

- Python 3.9+
- 1GB RAM minimum
- Playwright browsers installed
- Environment variables configured

## Security Notes

- All credentials encrypted with AES-256
- Sessions auto-expire after 7 days
- Anti-detection measures applied by default
- Audit logging enabled
