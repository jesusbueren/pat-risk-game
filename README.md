# 👽 Pat the Alien: Risk & Choice Experiment

An interactive web-based classroom experiment designed to explore economic decision-making under the **Veil of Ignorance**. Students play a game where their choices reveal their coefficient of relative risk aversion ($\sigma$), which is then aggregated onto a live teacher dashboard.

## 🚀 Live Access
* **The Game:** (https://jesusbueren.github.io/pat-risk-game/)
* **Teacher Dashboard:** (https://jesusbueren.github.io/pat-risk-game/results)

---

## 🛠 Features

### 1. The Game (`index.html`)
* **Interactive Narrative:** Students make life choices for "Pat the Alien" without knowing which world they will inhabit.
* **Risk Calculation:** Uses student choices to calculate an individual risk aversion score ($\sigma$).
* **Real-time Submission:** Data is sent instantly to a Google Sheets backend via the Google Apps Script API.

### 2. Analytics Dashboard (`dashboard.html`)
* **Live Statistics:** Displays the class average using the formula:
  $$\bar{\sigma} = \frac{1}{n} \sum_{i=1}^{n} \sigma_i$$
* **Visual Distribution:** A real-time bar chart (Chart.js) showing the spread of risk profiles from "Risk Taker" to "Cautious."
* **Data Management:** * **Download CSV:** Export student results for further analysis in Excel or R.
    * **Clear Data:** Reset the spreadsheet directly from the dashboard for the next class period.

---

## 📊 Technical Stack
* **Frontend:** HTML5, CSS3 (Flexbox/Grid), JavaScript (ES6+).
* **Math Rendering:** [MathJax](https://www.mathjax.org/) for high-quality LaTeX economic notation.
* **Data Visualization:** [Chart.js](https://www.chartjs.org/) for the distribution histogram.
* **Backend:** Google Apps Script (Web App) connected to Google Sheets.

---

## ⚙️ Setup & Deployment

1. **Google Sheets Integration:**
   * Create a Google Sheet with headers: `Name`, `Empty`, `Game`, `Sigma`, `Status`, `Timestamp`.
   * Deploy the provided `doPost` script as a Web App (set access to "Anyone").
   * Paste the deployment URL into the `DATA_URL` variable in both `index.html` and `dashboard.html`.

2. **GitHub Pages:**
   * Enable GitHub Pages in the repository settings.
   * Ensure `index.html` (the game) and `dashboard.html` (the analytics) are in the root folder.

---

## 📝 Notation Guide
In this experiment, we define:
* $\sigma_i$: The individual risk aversion coefficient for student $i$.
* $n$: The total number of participants.
* $\bar{\sigma}$: The arithmetic mean of the class's risk profile.

---

*Created for educational purposes to demonstrate economic principles and behavioral choice.*
