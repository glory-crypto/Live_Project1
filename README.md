# Live_Project1
# Bangalore Tech Salary Decoder 🚀

An end-to-end data analytics project built to inspect, clean, and analyze a messy real-world dataset of **1,000+ Bengaluru tech professionals**. This project skips the generic industry averages to provide exact quantitative insights broken down by roles, experience bands, organizational structures, and core skill requirements.

## 📊 Project Overview
Job seekers frequently rely on guesswork or crowdsourced sheets when benchmark-testing their target compensation (CTC). This project provides a robust, data-backed approach to tech salary intelligence by implementing systematic data cleaning and exploratory data analysis using **Python and Pandas** without relying on advanced external libraries or regex parsing.

## 🔑 Key Insights Uncovered
* **The Unicorn Premium:** Growth-stage Unicorn startups pay a massive premium, offering a median of **27.4 LPA** for SDE Backend talent—a **33.7% compensation jump** over traditional MNC architectures (**20.5 LPA**).
* **The Architecture Gate:** Mastering system design scales your value. Software engineers possessing **System Design** capabilities command a median package of **25.3 LPA** vs **21.0 LPA** without it, locking in a **+4.3 LPA standalone skill premium**.
* **The Junior Inflection Point:** The most aggressive percentage trajectory jump occurs at the early career milestone. SDE Backend professionals with 2-3 years of experience hit a median of **20.0 LPA**, yielding a staggering **71.7% increase** over entry-level freshers (**11.7 LPA**).

---

## 🛠️ Pipeline Architecture & Project Workflow
The notebook follows a strict modular progression from a raw dirty CSV file to a cleanly formatted console dashboard:

### 📋 Phase 1: Load & Inspect (`TASK 1`)
* Evaluated structural constraints of the raw file, showing a baseline shape of **1,015 rows × 12 columns**.
* Isolated missing value distributions (identifying ~19.7% null entries in historical metrics like `Previous_CTC`, matching the expected profile for freshers).
* Recognized that critical compensation columns were stored as string objects with erratic formatting.

### 🧼 Phase 2: Data Preprocessing & Cleaning (`TASK 2`)
* Standardized column headers into normalized `snake_case`.
* Mapped 40+ highly fragmented role variants into 7 canonical job classifications (e.g., merging `BE`, `Backend Dev`, and `Backend Developer` into `SDE Backend`).
* Cleaned complex financial string metrics (handling formats like `'41.4 LPA'`, `'3,360,000'`, and `'₹10.0 LPA'`) into uniform float variables representing **LPA** units using native string methods.
* Handled duplicate records and safely resolved missing nominal data.

### 📈 Phase 3: Business Logic Analytics Questions (`TASK 3`)
* **Q3.1:** Compiled statistical distributions (median, mean, min, max) for every role type, identifying Product Managers as the top earners.
* **Q3.2:** Constructed SDE Backend experience curves using specialized custom interval data cuts (`pd.cut`).
* **Q3.3:** Evaluated explicit premium value adds for target engineering skill arrays using string containment filters.
* **Q3.4 & Q3.5:** Grouped salary scales and compound switch jump increment percentages (averaging **38.7% overall**) across varying business tiers.

### 🖼️ Phase 4: Structured ASCII Summary Output Report (`TASK 4 & 5`)
* Renders a custom terminal chart dashboard leveraging localized padding layouts and block-bars (`█`) to provide an instant, scannable snapshot of the market data.

---

## 🚀 Getting Started

### Prerequisites
Make sure you have `pandas` and `numpy` installed on your machine:
```bash
pip install pandas numpy
