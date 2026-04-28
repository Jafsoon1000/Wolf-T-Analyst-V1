# 🐺 Wolf Terminal V1 (MSnR Intelligence)

![Status](https://img.shields.io/badge/Status-Active-brightgreen) ![Version](https://img.shields.io/badge/Version-1.0.0-blue) ![License](https://img.shields.io/badge/License-MIT-green)

Wolf Terminal V1 is a highly sophisticated, dark-themed market analysis dashboard and trading bot interface designed for precision snipers. Built around the proprietary **MSnR (Market Support & Resistance) Protocol**, this terminal provides real-time visualizations of critical market levels, trading setups, and asset pricing.

## 🚀 Key Features

*   **Live Market Intelligence:** Integrated TradingView widgets provide real-time ticker tape and interactive charts (Default focus: XAUUSD - Gold).
*   **Dynamic Data Syncing:** Connects seamlessly with a backend bot via `data.json` to stream live support (V), resistance (A), and trade signal biases directly to the dashboard.
*   **Level Freshness Scanner (The Lab):** An interactive diagnostic tool that visually scans and verifies if a structural bone (level) has been pierced (used) or remains fresh for a high-probability trade.
*   **Setup Registry:** Built-in documentation and guidelines for advanced MSnR setups:
    *   *Breakout MSnR* (High Probability)
    *   *Classic SnR* (Standard)
    *   *HNS Precision* (Trend Flip)
    *   *BHNS Trap* (Advanced)
*   **Cyberpunk/Terminal Aesthetic:** Built with Tailwind CSS, featuring a sleek, responsive dark mode design with glowing neon accents (Wolf Green, Wolf Red, and Wolf Gold).

## 🛠️ Tech Stack

*   **Frontend:** HTML5, Tailwind CSS, Vanilla JavaScript
*   **Charting & Visualization:** Chart.js, HTML5 Canvas API
*   **Market Data Widgets:** TradingView External Embeds
*   **Backend / Bot Integration:** Designed to interface with a Python-based trading algorithm using local JSON data exchange.

## 📂 Project Structure

```text
Wolf-T-Analyst-V1/
├── index.html      # Main terminal dashboard interface
├── README.md       # Project documentation (You are here)
├── data.json       # Live bot data stream (Support, Resistance, Bias)
└── levels.json     # Stored historical/scanned levels data
```

## ⚙️ Getting Started

### Prerequisites
You only need a modern web browser to view the frontend interface. To utilize the bot integration properly, a local server environment is recommended to avoid CORS issues when fetching the local JSON files.

### Installation & Usage

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/Jafsoon1000/Wolf-T-Analyst-V1.git
    cd Wolf-T-Analyst-V1
    ```

2.  **Launch the Dashboard:**
    *   *Option A (Simple):* Open `index.html` directly in your web browser. *(Note: Fetching `data.json` might be blocked by CORS policies if opened via `file://`)*.
    *   *Option B (Recommended):* Run a local web server.
        *   Using Python: `python -m http.server 8000`
        *   Using VS Code: Install and start the **Live Server** extension.
    *   Navigate to `http://localhost:8000` (or the port provided by Live Server) to view the terminal.

3.  **Bot Integration (Data Sync):**
    *   The frontend automatically pings `data.json` every 30 seconds to fetch live terminal metrics. 
    *   Configure your Python trading bot to write its current analysis to `data.json` using the expected format:
        ```json
        {
          "support_v": "2310.50",
          "resistance_a": "2345.80",
          "last_signal": "BUY"
        }
        ```

## 🎯 Project Roadmap

- [x] Build the Web Terminal for Daily Market Analysis.
- [ ] Develop and link the Python-based Trading Bot backend.
- [ ] Implement secure user authentication for personalized dashboard settings.
- [ ] Add historical backtesting visualizer.

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to fork this project and submit a pull request.

## 📜 License

This project is open-source and available under the MIT License.
