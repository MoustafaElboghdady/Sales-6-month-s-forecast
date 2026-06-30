# Sales Forecasting — 6-Month Customer Demand Prediction

**Forecasting weekly customer volume for Orient Group using historical trends and seasonality, to support planning and resource allocation.**

📍 Tourism & Travel Sector | Real production data (20,900+ records, 2023–2026)

---

## 📊 Project Overview

This project predicts how many customers Orient Group can expect each week for the next 6 months. Instead of relying on guesswork or last year's averages, the forecast is built from three years of actual transaction history and accounts for both seasonal patterns and recent momentum in customer activity.

**The goal:** give management an early, data-backed view of upcoming demand so staffing, marketing, and operations can be planned ahead of time instead of reacting after the fact.

---

## 🎯 Business Question

*Based on past customer behavior, how many customers should we expect each week for the next 6 months — and which months need the most attention?*

---

## 🛠️ Approach (Plain-English Summary)

1. **Collected and cleaned 3 years of real transaction data** (2023 – May 2026), removing duplicates and fixing data formatting issues.
2. **Counted customers per week** to build a clean weekly timeline of demand.
3. **Identified two key drivers of customer volume:**
   - **The season (month):** some months are naturally stronger or weaker.
   - **Recent momentum:** how many customers came in the past 1–2 weeks, since demand doesn't reset to zero — it carries forward.
4. **Built a forecasting model** that learns from these patterns and tested it against real historical data to check its accuracy.
5. **Generated a 6-month forecast** with weekly and monthly customer predictions, including a realistic best-case / worst-case range.

---

## 📈 Key Results

### Model Quality

| Metric | Result | What it means |
|---|---|---|
| **Accuracy (R²)** | 68% | The model explains 68% of the variation in weekly customer counts — solid for a business with many outside influencing factors (pricing, promotions, competitor activity, etc.) |
| **Average error per week** | ~63 customers | On a typical week, the forecast is off by about 63 customers in either direction |
| **Typical % error** | ~49% | Error is proportionally larger in slow weeks with low customer counts, and proportionally smaller in busy weeks — this is normal for week-level forecasting and improves significantly when looking at monthly totals |

> **Takeaway:** The model is reliable for spotting *trends and seasonal patterns* — which months to prepare for, and the general direction demand is heading. It is best used for **planning purposes**, not as an exact daily/weekly guarantee.

---

### Seasonality — Which Months Are Strongest?

Using three years of history, the model identified a clear, repeating seasonal pattern:

| Performance | Months |
|---|---|
| 🟢 **Strongest** | April, November |
| 🟡 **Moderate** | August, January, October |
| 🔴 **Weakest** | February, March, June, July, September |

**Business implication:** April and November consistently bring in the most customers — these are the best windows for promotional pushes and upselling. February and March are historically the slowest months, making them good candidates for retention campaigns or cost optimization instead of aggressive customer acquisition spend.

---

### Year-over-Year Growth

The data shows a **steady underlying growth trend** in customer volume year after year, independent of seasonal swings. This confirms the business is growing organically, not just riding seasonal cycles.

---

## 📅 6-Month Forecast (Monthly Totals, with 95% Confidence Range)

| Month | Expected Customers | Likely Range (Low – High) |
|---|---|---|
| June | 1,271 | 942 – 1,600 |
| July | 1,267 | 938 – 1,596 |
| August | 2,041 | 1,673 – 2,409 |
| September | 1,311 | 982 – 1,640 |
| October | 1,355 | 1,026 – 1,684 |
| November | 1,325 | 1,040 – 1,610 |

**Reading the range:** the "Low – High" columns represent a realistic band — there's a 95% chance the actual number falls within this range. This helps with planning for both a conservative and an optimistic scenario rather than relying on a single fixed number.

---

## 📉 Visual Summary

The project includes two key charts:

1. **Weekly Forecast Trend** — a week-by-week view of expected customer volume across the next 6 months, showing the natural rise and fall through each season.
2. **Monthly Forecast with Confidence Range** — a shaded-band chart showing the expected monthly total alongside the realistic best/worst-case range, making it easy to communicate uncertainty to stakeholders at a glance.

*(Charts are available in the project notebook / exported images.)*

---

## 💡 Recommendations

1. **Align staffing and marketing budget with the seasonal calendar** — scale up around April and November, scale down or shift focus during February–March.
2. **Re-run the forecast monthly** as new data comes in, so predictions stay current rather than static.
3. **Use the confidence range, not just the single number,** when presenting to leadership — it sets realistic expectations and avoids over-promising.
4. **Enhance the model over time** by adding more business drivers (marketing spend, pricing changes, competitor activity, promotions calendar) to improve accuracy further.
5. **Connect the forecast output to a live dashboard** (Power BI) so the latest predictions are always visible to decision-makers without manual updates.

---

## 🤝 Tools & AI Usage

This project — data cleaning, feature engineering, model building, and evaluation — was built and coded independently. AI assistance was used for one specific part: optimizing the code that calculates the 95% confidence interval (lower/upper bound) for the forecast. The logic and forecasting approach are mine; AI helped streamline that particular block of code.

---

## 🛠️ Technical Stack

| Tool | Purpose |
|---|---|
| Python (pandas, numpy) | Data cleaning & weekly aggregation |
| statsmodels | Forecasting model & statistical validation |
| scikit-learn | Model accuracy evaluation |
| matplotlib / seaborn | Visualization |
| VS Code + Jupyter | Development environment |

---

## 📁 Data

- **Source:** Internal transaction system (Orient Group)
- **Size:** 20,900+ customer records
- **Time range:** 2023 – May 2026
- **Granularity:** Aggregated to weekly customer counts for forecasting

---

## 🎓 What This Project Demonstrates

- Translating raw transactional data into a forward-looking business tool
- Statistical forecasting with transparent accuracy reporting (no inflated claims)
- Communicating uncertainty responsibly (confidence ranges, not false precision)
- End-to-end workflow: data cleaning → feature engineering → model validation → business-ready output

---

*Project Date: June 2026 — Orient Group, Tourism & Travel Sector*
