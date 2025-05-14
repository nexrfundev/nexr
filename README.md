# NEXR
![image](https://github.com/user-attachments/assets/0a891b39-08df-440b-a3ac-f2c63e3d9483)

**Tokenize Anything. Tokenize Everything.**

# NEXR 

**Tokenize Anything. Tokenize Everything.**

NEXR is a Chrome extension that lets you launch memecoins from **tweets**, **articles**, and **any content online** with a single click. Built on **Solana** and deployed instantly via **Pump.fun**, NEXR removes all friction from memecoin creation.

---

##  How It Works

1. **Highlight any tweet, post, or news article**  
2. **Click the NEXR extension**  
3. NEXR extracts the **title**, **image**, and **description** using AI  
4. Set your **initial investment** and **launch** the token on Pump.fun  
5. Go viral.

---

##  Features

-  **One-Click Tokenization** – Turn content into tokens instantly  
-  **AI Metadata** – Auto-generated titles, images, and descriptions  
-  **Built-in Wallet** – Manage your Solana wallet directly in the extension  
-  **Custom Image Upload** – Use your own art or pull directly from source  
-  **Developer Preview Mode** – Test launches with custom prompts  
-  **Leaderboard & History** – Track performance of your launches  
-  **Cross-Platform** – Works on Twitter, X, Reddit, Medium, and more

---

##  Installation

1. Clone the repo:
```bash
git clone https://github.com/yourusername/nexr.git
2. Install dependencies:
cd nexr
npm install
3. Build the extension:
npm run build
4. Load in Chrome:
- Go to chrome://extensions/
- Enable Developer Mode
- Click Load Unpacked
- Select the /dist folder


Project Structure
nexr/
├── public/
├── src/
├── scripts/
├── assets/
├── tests/
├── sidebar.html
├── manifest.json
├── package.json
├── tailwind.config.js
├── tsconfig.json
└── ...

Roadmap
 MVP (token creation from text/images)
 Wallet + investment amount config
 Extension Store Release
 Leaderboard API integration
 Social sharing features

Try It Soon
 The extension will be available on the Chrome Web Store shortly.
 Join the $NEXR community and be the first to mint your memes into memecoins.

License
MIT

Architecture

graph LR
  subgraph "Chrome Extension"
    CS["Content Script"]
    BG["Background Service Worker"]
    UI["React Popup UI"]
    Store["Zustand Store"]
  end

  subgraph "External Services"
    AI["Token Creation API"]
    PumpFun["Pump.fun API & IPFS"]
    Solana["Solana Blockchain"]
    Firebase["Firebase Analytics"]
  end

  CS -->|Extract content| BG
  UI -->|User actions| BG
  BG -->|State updates| Store
  BG -->|Generate metadata| AI
  BG -->|Upload metadata| PumpFun
  BG -->|Create & fund tokens| Solana
  BG -->|Log events| Firebase
  Store -->|State| UI
