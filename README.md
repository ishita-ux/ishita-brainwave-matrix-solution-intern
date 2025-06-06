PhishScan — Phishing URL Scanner Tool

PhishScan is a powerful **Python-based phishing URL scanner** designed to detect potentially harmful phishing links with advanced analysis techniques. It helps users and security researchers identify phishing threats by checking multiple parameters such as SSL certificate details, domain age, blacklist presence, URL patterns, and more. The tool presents the scan results in a clean, easy-to-read table format enhanced with intuitive emojis and warnings to quickly highlight suspicious features.

---

## Features

- Detects if URL uses HTTPS with a caution that HTTPS doesn’t guarantee safety  
- Fetches and analyzes SSL certificate details like issuer, common name, and expiry date  
- Checks domain age using WHOIS data to identify recently created (suspicious) domains  
- Identifies if the domain is in a predefined blacklist of known phishing or malicious domains  
- Detects use of IP addresses instead of domain names in URLs  
- Checks for URL encoding, '@' symbol usage, and URL length that are common in phishing URLs  
- Displays all findings in a formatted table with clear status and warnings  

---

## How to Download and Use

### 1. Clone the Repository

Open your terminal or command prompt and run:

```bash
git clone https://github.com/ishita-ux/PhishScan.git
cd PhishScan
2. Install Dependencies

Make sure you have Python installed (version 3.6+ recommended). Then install required packages:

pip install -r requirements.txt

3. Run the Scanner

Run the main Python script:

python main.py

You will be prompted to enter a URL for scanning. The tool will then perform checks and display the results in a colorful, emoji-enhanced table.
Example Usage

🔗 Enter URL to scan: https://example-phishing-site.com

📋 Scan Summary:
╒═════════════════════════════╤════════════════════════════════╕
│ Feature                     │ Result                         │
╞═════════════════════════════╪════════════════════════════════╡
│ 🔐 HTTPS Used               │ Yes (⚠️ Can still be phishing) │
│ 🔒 SSL Issuer               │ Let's Encrypt                  │
│ 📛 Certificate CN           │ example-phishing-site.com      │
│ 📆 SSL Expiry Date          │ 2025-06-20                     │
│ ⏳ Days Until Expiry        │ 14 days                        │
│ ⚠️ SSL Warning              │ Certificate expires soon!      │
│ 🚫 Blacklisted Domain       │ No                            │
│ 🌐 Domain Name             │ example-phishing-site.com      │
│ 📡 Resolved IP              │ 192.0.2.1                     │
│ ⚠️ Uses IP Instead of Domain │ No                            │
│ ⚠️ URL Contains Encoding    │ No                            │
│ 📏 URL Length > 75          │ No                            │
│ ⚠️ Contains '@' Symbol      │ No                            │
│ 📅 Domain Age               │ 120 days (Young)               │
╘═════════════════════════════╧════════════════════════════════╛

Contributions

Feel free to fork the repository, suggest improvements, or add features via pull requests.
License

This project is open-source and free to use.

Made with ❤️ by Ishita Arya
