# Library Late Return Analysis

This project analyzes library checkout data to find the main reasons for late book returns. The goal was to clean the raw data using Python and build an interactive Power BI dashboard to present the findings and suggest solutions.

---

## Data Cleaning (Python)

I merged and cleaned four separate CSV files (`checkouts`, `customers`, `books`, `libraries`) to create a single, trustworthy master dataset for analysis.

* **Date Validation:**
    * Removed illogical records (e.g., books returned before checkout).
    * Filtered the data to a modern timeframe (2005-present).

* **Text Standardization:**
    * Cleaned and standardized all text fields (names, addresses, categories) for consistency.

* **Data Quality Flag:**
    * Instead of deleting rows with errors (like an invalid ZIP code or a birth date from before 1930), I created a `data_quality` flag. This preserves all data while allowing for accurate, filtered analysis.

* **Final Merge:**
    * Combined the four cleaned files into a single master file, ready for Power BI.

---

## Key Findings (Power BI)

The interactive dashboard revealed three clear patterns driving late returns:

* **Geography Matters:** Patrons living in the city's outskirts have a much higher late return rate, suggesting that **distance** and **travel convenience** are major factors.

* **Demographics Show Clear Trends:** The **60+ age group** and **male patrons** are significantly more likely to return books late.

* **Book Type Plays a Role:** **Longer books** (over 700 pages), more **expensive books** (over $500), and books from specialized academic categories are all returned late more often.

---

## Recommendations

Based on the data, I recommend a targeted approach rather than a one-size-fits-all solution:

* **Make Returns Easier:** Introduce a **"Return to Any Branch"** policy to help patrons who live far from their home library.

* **Support Senior Patrons:** Pilot a **"Library at Home"** pickup/drop-off service for the 60+ age group and offer non-digital reminder options like automated phone calls.

* **Create Smart Policies:** For long or expensive books, test a **longer loan period** (e.g., 35 days) and send more proactive, content-aware reminders.
