# 🌟 WordWeaver Bot

**An intelligent daily vocabulary companion that weaves English words with Dutch translations**

[![n8n](https://img.shields.io/badge/n8n-automation-FF6D5A?style=flat-square)](https://n8n.io)
[![OpenAI](https://img.shields.io/badge/OpenAI-GPT--4-412991?style=flat-square)](https://openai.com)
[![Discord](https://img.shields.io/badge/Discord-webhook-5865F2?style=flat-square)](https://discord.com)
[![Google Sheets](https://img.shields.io/badge/Google-Sheets-34A853?style=flat-square)](https://sheets.google.com)

---

## ✨ What is WordWeaver?

WordWeaver is an automated language learning bot that picks a random English word from your Google Sheet every day, uses AI to find related words, translates them to Dutch, and shares the knowledge through Discord while building your vocabulary database.

### 🎯 Perfect for:
- Language learners building vocabulary
- Discord communities focused on learning
- Automated daily educational content
- Building comprehensive word databases

---

## 🚀 Features

🔄 **Daily Automation** - Runs every morning at 9:00 AM  
🤖 **AI-Powered** - Uses GPT-4 to find semantically related words  
🇳🇱 **Dutch Translations** - Automatic translation for each word  
📊 **Google Sheets Integration** - Reads source words and saves results  
💬 **Discord Notifications** - Beautiful embedded messages  
📈 **Progressive Learning** - Builds your vocabulary database over time  
🛡️ **Error Handling** - Robust error management and fallbacks  

---

## 🏗️ Architecture

```
Google Sheets → n8n Workflow → OpenAI GPT-4 → Discord + Database Update
     ↑                                              ↓
   [Source Words] ←------------------------→ [Generated Words]
```

**Workflow Steps:**
1. 📅 Daily trigger activates
2. 📖 Reads random word from Google Sheet
3. 🧠 AI generates 10 related words with context
4. 🌍 Translates each word to Dutch
5. 💬 Sends formatted message to Discord
6. 💾 Saves results to Google Sheets database

---

## ⚡ Quick Start

### Prerequisites
- [n8n](https://n8n.io) instance (cloud or self-hosted)
- OpenAI API key
- Google Sheets API access
- Discord webhook URL

### Setup
1. **Clone & Import**
   ```bash
   git clone https://github.com/yourusername/wordweaver-bot.git
   ```

2. **Import to n8n**
   - Copy the workflow JSON
   - Import into your n8n instance

3. **Configure Credentials**
   - Add OpenAI API credentials
   - Set up Google Sheets OAuth2/Service Account
   - Create Discord webhook in your channel

4. **Customize**
   - Update Google Sheet ID in workflow
   - Set your Discord webhook URL
   - Adjust the daily schedule if needed

5. **Activate & Enjoy!** 🎉

---

## 📋 Example Output

**Discord Message:**
```
📚 Daily English Word: Kitchen

Category: **Cooking**

🇳🇱 Related Words with Dutch Translations
1. **stove** → fornuis
2. **refrigerator** → koelkast  
3. **oven** → oven
4. **pan** → pan
5. **knife** → mes
...

Generated on January 16, 2025
```

**JSON Structure:**
```json
{
  "category": "cooking",
  "related_words": [
    {"dutch": "fornuis", "english": "stove"},
    {"dutch": "koelkast", "english": "refrigerator"}
  ],
  "error": ""
}
```

---

## 🛠️ Configuration

| Setting | Description | Default |
|---------|-------------|---------|
| Schedule | When to run daily | 9:00 AM |
| Word Count | Related words to generate | 10 |
| Discord Limit | Words shown in Discord | 8 |
| Sheet Name | Source words sheet | Sheet1 |
| Output Sheet | Generated words storage | Generated_Words |

---

## 🤝 Contributing

We love contributions! Whether it's:
- 🐛 Bug fixes
- ✨ New features  
- 📝 Documentation improvements
- 🌍 Additional language support

Feel free to open an issue or submit a pull request!

---

## 📄 License

MIT License - feel free to use this for your own learning adventures!

---

## ⭐ Show Your Support

If WordWeaver helps you learn new words, give it a star! ⭐

**Happy learning!** 🎓✨