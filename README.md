# 📱 Social Media Management System — Multi-Agent AI

> *Understand what the internet is saying — automatically.*

A multi-agent system that scrapes Reddit, analyzes sentiment, surfaces trending themes, and generates shareable reports — all through a live Streamlit dashboard.

---

## 🚀 Quick Start

```bash
# Clone the repo
git clone https://github.com/Bilal-Ahmad-5/Social-Media-Management-System.git
cd Social-media-Agent

# Set up environment
python -m venv venv
source venv/bin/activate        # macOS/Linux
venv\Scripts\activate           # Windows

# Install dependencies
pip install -r requirements.txt
```

Create a `.env` file with your Reddit credentials:

```
REDDIT_CLIENT_ID=your_client_id
REDDIT_CLIENT_SECRET=your_client_secret
REDDIT_USER_AGENT=your_app_name
```

> Get Reddit API credentials free at [reddit.com/prefs/apps](https://www.reddit.com/prefs/apps)

Then launch the dashboard:

```bash
streamlit run app.py
```

---

## ✨ What It Does

| Feature | Description |
|---------|-------------|
| 🕷️ **Reddit Scraper** | Pulls posts and comments from any subreddit |
| 💬 **Sentiment Analysis** | Classifies posts as positive, negative, or neutral |
| 🏷️ **Theme Extraction** | Groups posts by topic to surface what people care about |
| 📊 **Report Generator** | Builds trend charts, theme breakdowns, and exportable reports |

---

## 🧠 How It Works

Four focused agents handle the pipeline end-to-end:

| Agent | Job |
|-------|-----|
| 🕷️ **Scraper Agent** | Fetches Reddit posts with rate-limit handling |
| 💬 **Sentiment Agent** | HuggingFace transformers (falls back to keyword scoring on CPU) |
| 🏷️ **Theme Tagger Agent** | Extracts and groups common topics from post text |
| 📝 **Report Agent** | Aggregates everything into charts and downloadable reports |

**LangGraph** orchestrates the full flow: `scrape → analyze → tag → report`

---

## ⚙️ Requirements

- Python 3.8+
- Reddit API credentials (free) → [reddit.com/prefs/apps](https://www.reddit.com/prefs/apps)
- GPU optional — runs on CPU with keyword fallback

---

## 💡 Tips for Best Results

- **Start small** — test with 1–2 subreddits and a short time window first
- **No GPU?** The keyword-based fallback analyzer works well on any machine
- **Watch the logs** in the dashboard to catch rate limits early

---

## 🔮 What's Coming Next

- Persistent storage for historical trend tracking
- Scheduled recurring scrape runs
- Multi-user team dashboards with authentication
- Support for Twitter/X, Mastodon, and more platforms

---

## 🤝 Contributing

Fork it, build something useful, open a pull request. All contributions welcome.

---

## 📄 License

MIT — free to use and build upon.
