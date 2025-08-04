# 🧠 Trader Behaviour

"Mutual funds are subject to market risks", yet no one reads the scheme related documents carefully :( No worries ! I got you covered. Here's a sentiment‑aware analysis of trader behaviour using *Fear vs. Greed* index and historical trade execution data.

---

## 🎯 Objective

To explore how Bitcoin market sentiment influences trader behaviour—such as profitability, trade direction, and size—and uncover actionable insights based on patterns across emotion-driven phases.

---

## 📂 Datasets

- **historical_data.csv** (or similarly named): Contains individual trade records—fields like account, coin, execution price, trade size (USD), closed PnL, timestamp, side (Buy/Sell), etc.  
- **fear_greed_index.csv**: Contains daily market sentiment labels (Fear vs. Greed) and sentiment score where available.

---

## ⚙️ Data Workflow

1. **Preprocessing**
   - Parse and convert timestamps into datetime.
   - Merge sentiment and trade data by date.
   - Clean columns and handle missing values.

2. **Exploratory Data Analysis (EDA)**
   - Compute average and median Closed PnL under Fear vs. Greed.
   - Calculate win rate (# profitable trades / total) by sentiment.
   - Explore trade size distribution across sentiment.
   - Compare Buy vs. Sell performance per sentiment.

3. **Visualization**
   - Generate bar charts, boxplots, and distribution plots summarizing the above metrics.

---

## 📈 Key Insights

- Traders tend to perform better during **Greed** periods (higher average PnL and win rates).
- During **Fear**, trade outcomes are more volatile, with cautious behaviour dominating.
- Trade direction interacts with sentiment: e.g. Buy or Long trades may do better in Greed and Sell or Short trades may yield more in Fear.
- Larger trade sizes often appear in Greed—indicating greater confidence.
- Top-performing accounts/traders are more active in Greed phases, suggesting momentum-based strategies.

---

## 📝 Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/sudiptasarkar011/trader-behaviour.git
   cd trader-behaviour
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Place your datasets under a `data/` folder, e.g.:
   ```
   data/historical_data.csv
   data/fear_greed_index.csv
   ```
4. Open and run the main analysis notebook (e.g., `analysis.ipynb` or similar) to reproduce results and visualizations.

---

## 🔍 Insights & Applications

- Align trading strategy (direction, size, timing) with daily sentiment context.
- Increase trading activity in Greed phases; cautiously limit exposure during Fear.
- Model or automate signals that capitalize on sentiment shifts.
- Use these insights to build smarter, sentiment-aware trading systems or dashboards.

---

## 💻 Tools Used

- Python (Pandas, NumPy)
- Jupyter Notebook (or Google Colab)
- Matplotlib / Seaborn for visualizations

---


