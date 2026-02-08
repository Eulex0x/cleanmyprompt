# Clean My Prompt 🔒

**Privacy-First AI Prompt Sanitizer - Remove Sensitive Data Before Sharing**

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Client-Side](https://img.shields.io/badge/Processing-100%25%20Client--Side-blue.svg)]()
[![Privacy](https://img.shields.io/badge/Privacy-Zero%20Data%20Collection-brightgreen.svg)]()

🌐 **[Live Demo: CleanMyPrompt.com](https://cleanmyprompt.com)**

---

## 🚀 What is Clean My Prompt?

Clean My Prompt is a **100% client-side web tool** that sanitizes sensitive data from text before you share it with AI assistants like ChatGPT, Claude, or Gemini. It detects and replaces emails, API keys, passwords, credit cards, phone numbers, IP addresses, names, and more—**all in your browser's memory**.

### ✨ Key Features

- **🔐 100% Offline Processing** - Zero network requests after page load
- **🧠 Smart NLP Detection** - Uses Compromise.js to detect names, places, companies
- **🌍 International Support** - Handles US, EU, and German data formats
- **⚡ Real-Time Sanitization** - Updates as you type
- **🎨 Two Modes** - Placeholder mode (`[EMAIL_1]`) or Realistic mode (`user@company.com`)
- **🔧 Custom Patterns** - Add your own regex patterns for domain-specific data
- **🎯 15+ Detection Patterns** - Emails, URLs, IPs (v4/v6), phones, credit cards, IBANs, API keys, credentials
- **📖 Open Source (MIT)** - Fully auditable, fork-friendly

---

## 🎯 Why Use This?

### The Problem
Developers and professionals accidentally leak sensitive data when using AI assistants:
- 🔑 API keys and secrets in debugging prompts
- 📧 Customer emails in support tickets
- 💳 Credit card numbers in payment troubleshooting
- 🏢 Real names and locations in document drafts
- 🌐 Server IPs and database credentials

### The Solution
**One-click sanitization** that works entirely in your browser. No trust required—verify in DevTools that zero network requests are made.

---

## 🛠️ How It Works

1. **Paste** your text containing sensitive data
2. **Watch** real-time sanitization (no button needed!)
3. **Copy** the cleaned output to clipboard
4. **Share** safely with AI assistants

### Technical Architecture

```
User Input → Browser RAM → NLP Analysis → Regex Matching → Sanitized Output
                ↓
         No Network I/O
         No Server Storage
         No Data Persistence
```

**Detection Pipeline:**
1. **NLP First:** Compromise.js detects people, places, organizations
2. **Regex Second:** 15+ patterns catch structured data (emails, IPs, keys, etc.)
3. **Instant Output:** Sanitized text generated in milliseconds

---

## 📦 What Gets Detected?

| Category | Examples | Formats |
|----------|----------|---------|
| 📧 **Emails** | `user@example.com`, `john.doe+tag@company.io` | Universal |
| 📞 **Phones** | `(555) 123-4567`, `+49 176 1234567`, `0176265124` | US, EU, DE |
| 🔑 **API Keys** | `sk_live_abc...`, `AKIAIOSFODNN7...`, `ghp_xyz...` | AWS, GitHub, Stripe, generic |
| 🌐 **IPs** | `192.168.1.1`, `2001:0db8:85a3::8a2e:0370:7334` | IPv4, IPv6 |
| 💳 **Credit Cards** | `4532-1234-5678-9010`, `5425 2334 3010 9903` | Universal |
| 🏦 **IBANs** | `DE89370400440532013000`, `FR14 2004...` | EU |
| 🔐 **Credentials** | `password: abc123`, `username: admin` | Universal |
| 🔗 **URLs** | `https://api.example.com`, `www.site.com` | Universal |
| 👤 **Names** | `John Smith`, `Dr. Emily Chen` (NLP) | Universal |
| 🏢 **Companies** | `Microsoft`, `Apple Inc.` (NLP) | Universal |
| 📍 **Locations** | `Seattle`, `Berlin`, `Munich` (NLP) | Universal |

---

## 🖥️ Installation & Usage

### Option 1: Use Online (Recommended)
Visit **[CleanMyPrompt.com](https://cleanmyprompt.com)** - works immediately in any modern browser.

### Option 2: Run Locally
```bash
# Clone the repository
git clone https://github.com/yourusername/cleanmyprompt.git
cd cleanmyprompt

# Open in browser
open index.html  # macOS
start index.html # Windows
xdg-open index.html # Linux
```

No build process, no dependencies, no installation required!

### Option 3: Host Your Own
Upload all files to any static hosting:
- GitHub Pages
- Netlify
- Vercel
- AWS S3 + CloudFront
- Your own web server

---

## 🔒 Privacy & Security

### What We **DON'T** Collect
- ❌ Your prompts or sanitized text
- ❌ Personally identifiable information
- ❌ IP addresses
- ❌ User accounts
- ❌ Behavioral data
- ❌ Tracking cookies

### What We **DO** Collect
- ✅ Minimal anonymous analytics (country-level aggregates only)
- ✅ Page views (not who viewed them)

### Verification
1. Open browser DevTools (F12)
2. Go to **Network** tab
3. Paste sensitive text and sanitize
4. Observe: **Zero requests** after initial page load

**Offline Test:** Disconnect from the internet—the tool still works perfectly!

---

## 🌍 International Support

- 🇺🇸 **United States:** US phone formats, ZIP codes
- 🇩🇪 **Germany:** German phones (`0176...`), IBANs, postal codes
- 🇪🇺 **European Union:** IBAN validation, EU phone formats, GDPR compliance
- 🇬🇧 **United Kingdom:** UK phones, postal codes

Missing your region? [Open an issue](https://github.com/yourusername/cleanmyprompt/issues) or submit a PR!

---

## 🧪 Demo Data

Click **"Try Demo"** button in the app to load a comprehensive benchmark with 60+ test cases including:
- US & European phone numbers
- AWS, GitHub, and Stripe API keys
- IPv4 and IPv6 addresses
- Credit cards and IBANs
- Names, companies, and locations

---

## 🛣️ Roadmap

- [ ] Browser extension (Chrome, Firefox)
- [ ] CLI tool for terminal workflows
- [ ] Mobile PWA
- [ ] Import/export custom pattern libraries
- [ ] Advanced NLP models
- [ ] Multi-language UI

---

## 🤝 Contributing

Contributions welcome! Please:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

**Before submitting:**
- Test locally in multiple browsers
- Ensure no network requests during sanitization
- Update documentation if needed

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

**TL;DR:** Use freely, commercially or personally. Attribution appreciated but not required.

---

## 🙏 Credits

- **[Compromise.js](https://github.com/spencermountain/compromise)** - Client-side NLP
- **[Tailwind CSS](https://tailwindcss.com/)** - Utility-first CSS framework
- **Privacy advocates** - For pushing user-first design

---

## 📞 Support

- 🐛 **Bug Reports:** [GitHub Issues](https://github.com/yourusername/cleanmyprompt/issues)
- 💡 **Feature Requests:** [GitHub Discussions](https://github.com/yourusername/cleanmyprompt/discussions)
- 📖 **Documentation:** [Technical Deep Dive](https://cleanmyprompt.com/how-it-works.html)

---

## ⚖️ Legal

- [Privacy Policy](https://cleanmyprompt.com/privacy-policy.html)
- [Cookie Policy](https://cleanmyprompt.com/cookie-policy.html)
- [Terms of Service](https://cleanmyprompt.com/terms-of-service.html)

---

<div align="center">

**Made with ❤️ and respect for privacy**

[Website](https://cleanmyprompt.com) • [Technical Details](https://cleanmyprompt.com/how-it-works.html) • [About](https://cleanmyprompt.com/about.html)

⭐ Star this repo if it helps keep your data safe!

</div>

