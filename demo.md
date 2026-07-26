# RISHI — AI Assistant for Bharat 🌾🚆

**RISHI** (Rural India Support & Help Interface) is a comprehensive AI solution powered by a **NitroStack MCP Server** and debugged using **NitroStudio**. Designed specifically for rural, semi-literate, and first-time digital users across India, RISHI provides voice-first, multi-lingual access to essential public services, agricultural weather data, financial guidance, and scam protection.

---

## 🌟 Key Features

* **💰 Financial Assistance Advisor:** Guidance on Kisan Credit Card (KCC), Mudra loans, SHG loans, government subsidies, and PMFBY crop insurance.
* **📜 Government Schemes Analyzer:** Eligibility verification and step-by-step application procedures for PM-KISAN, Ayushman Bharat, MGNREGA, PMAY, and Ujjwala Yojana.
* **🌦️ Agri Weather & Soil Moisture Reporter:** Location-aware 5-day weather forecasts, total expected rainfall, and actionable seasonal crop advisories.
* **📘 Free Education Aggregator:** Discovers free courses and materials from NPTEL, SWAYAM, DIKSHA, and NCERT.
* **🛡️ Scam & Fraud Warning System:** Evaluates suspicious SMS texts, calls, and email links for red flags, returning instant risk scores and direct links to the National Cyber Crime Helpline (1930).
* **💼 Job Opportunity Finder:** Queries public sector recruitment channels (NCS, Employment News, SSC, RRB) for local employment opportunities.
* **⚡ Hybrid Model Engine (GPT-OSS 20B & Offline Lite Mode):** Runs via OpenRouter online using the lightweight **GPT-OSS 20B** model and automatically falls back to an instant zero-setup on-device "Lite" mode when offline.
* **🔊 Audio Dictation & Multilingual Voice UX:** Full Text-to-Speech (TTS) dictation and automatic support for all 22 official languages of India.

---

## 🔑 OpenRouter API Key Setup

1. Obtain a free API key from [OpenRouter](https://openrouter.ai/keys).
2. Launch the **RISHI** web interface (`index.html`) in your browser.
3. Click the **Settings (⚙️ Setup needed)** icon located in the top-right corner of the top bar.
4. Paste your API key (`sk-or-v1-...`) into the **OpenRouter API key** field.
5. Click **Save**. RISHI will use the free **GPT-OSS 20B** model for all dynamic online queries.

---

## 🗣️ Supported Languages

Supports seamless auto-detection and persistent switching across 22 Scheduled Indian languages + English:
`Assamese` • `Bengali` • `Bodo` • `Dogri` • `English` • `Gujarati` • `Hindi` • `Kannada` • `Kashmiri` • `Konkani` • `Maithili` • `Malayalam` • `Manipuri` • `Marathi` • `Nepali` • `Odia` • `Punjabi` • `Sanskrit` • `Santali` • `Sindhi` • `Tamil` • `Telugu` • `Urdu`

---

## 🏗️ Architecture Overview

                            +---------------------------+
                            |  RISHI Web Interface UI   |
                            |  (Voice / Text / TTS)     |
                            +-------------+-------------+
                                          |
                                  [ MCP Protocol ]
                                          |
                            +-------------v-------------+
                            |  NitroStack Server Engine |
                            +-------------+-------------+
                                          |
                   +----------------------+----------------------+
                   |                                             |
           (Online Mode)                                  (Offline Mode)
                   |                                             |
        +----------v----------+                       +----------v----------+
        | OpenRouter API      |                       | On-Device Lite /    |
        | (GPT-OSS 20B Model) |                       | WebGPU Local AI     |
        +----------+----------+                       +----------+----------+
                   |                                             |
                   +----------------------+----------------------+
                                          |
             +----------------------------v----------------------------+
             |                      NitroStack MCP                     |
             +----------+----------+----------+----------+-------------+
             | Financial| Schemes  | Weather  | Scam     | Education   |
             | Advisor  | Analyzer | Reporter | Defense  | & Jobs      |
             +----------+----------+----------+----------+-------------+

---

## ⚙️ Prerequisites

* **Node.js**: `>= 20.18.0`
* **npm**: `>= 9.0.0`
* **NitroStudio**: [Download NitroStudio IDE](https://nitrostack.ai/studio)

---

## 🚀 Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/rishi-mcp-server.git](https://github.com/your-username/rishi-mcp-server.git)
   cd rishi-mcp-server