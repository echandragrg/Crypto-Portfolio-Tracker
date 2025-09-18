**Crypto Portfolio Tracker**

A Tkinter-based desktop application to manage and track your cryptocurrency portfolio.
It fetches live crypto prices from the CoinMarketCap API
 and calculates profits/losses in real-time.

**Features**

Track Portfolio: View your holdings with live price updates.

P/L Calculation: Profit/Loss per coin and total P/L.

CRUD Support: Add, update, and delete coins from your SQLite database.

Refresh Option: Instantly refresh your portfolio with one click.

Clear Portfolio: Wipe all stored data and start fresh.

Simple UI: Built with Python’s Tkinter library.

**Screenshot**

<img width="1567" height="377" alt="image" src="https://github.com/user-attachments/assets/091868b6-8f05-47a3-9406-9185d5020e38" />


**Tech Stack**

Python 3

Tkinter (GUI framework)

SQLite3 (local database)

Requests + JSON (API handling)

CoinMarketCap API (live crypto prices)

Installation

Clone this repository:

git clone https://github.com/your-username/crypto-portfolio-tracker.git
cd crypto-portfolio-tracker


**Install dependencies:**

pip install requests


Add your CoinMarketCap API key
 in the code:

api_request = requests.get(
    "https://pro-api.coinmarketcap.com/v1/cryptocurrency/listings/latest?start=1&limit=300&convert=USD&CMC_PRO_API_KEY=YOUR_API_KEY"
)


**Run the app:**

python app.py

**Usage**

Add Coin → Enter symbol, price, and amount, then click Add Coin.

Update Coin → Enter portfolio ID, new values, and click Update Coin.

Delete Coin → Enter portfolio ID and click Delete Coin.

Clear Portfolio → Use the File → Clear Portfolio menu option.

Refresh → Refreshes portfolio values with live API data.

**Database**

The app uses SQLite with the following table:

CREATE TABLE IF NOT EXISTS coin(
    id INTEGER PRIMARY KEY,
    symbol TEXT,
    amount INTEGER,
    price REAL
);
