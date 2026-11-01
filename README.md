# India-Stocks-2611-2630-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 2611 to 2630)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-2611-2630-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (2611 to 2630)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 2611 | `XTRANET` | Xtranet Technologies Limited | `XTRANET.NS` |
| 2612 | `YASHO` | Yasho Industries Limited | `YASHO.NS` |
| 2613 | `YATHARTH` | Yatharth Hospital & Trauma Care Services Limited | `YATHARTH.NS` |
| 2614 | `YATRA` | Yatra Online Limited | `YATRA.NS` |
| 2615 | `YOGI` | Yogi Limited | `YOGI.NS` |
| 2616 | `YUKEN` | Yuken India Limited | `YUKEN.NS` |
| 2617 | `ZAGGLE` | Zaggle Prepaid Ocean Services Limited | `ZAGGLE.NS` |
| 2618 | `ZEELEARN` | Zee Learn Limited | `ZEELEARN.NS` |
| 2619 | `ZEEMEDIA` | Zee Media Corporation Limited | `ZEEMEDIA.NS` |
| 2620 | `ZENITHEXPO` | Zenith Exports Limited | `ZENITHEXPO.NS` |
| 2621 | `ZENITHSTL` | Zenith Steel Pipes & Industries Limited | `ZENITHSTL.NS` |
| 2622 | `ZETWERK` | Zetwerk Manufacturing Businesses Limited | `ZETWERK.NS` |
| 2623 | `ZFSTEERING` | ZF Steering Gear (India) Limited | `ZFSTEERING.NS` |
| 2624 | `ZIMLAB` | Zim Laboratories Limited | `ZIMLAB.NS` |
| 2625 | `ZODIAC` | Zodiac Energy Limited | `ZODIAC.NS` |
| 2626 | `ZODIACLOTH` | Zodiac Clothing Company Limited | `ZODIACLOTH.NS` |
| 2627 | `ZOTA` | Zota Health Care LImited | `ZOTA.NS` |
| 2628 | `ZSARACOM` | Saraswati Commercial India Limited | `ZSARACOM.NS` |
| 2629 | `ZUARI` | Zuari Agro Chemicals Limited | `ZUARI.NS` |
| 2630 | `ZUARIIND` | ZUARI INDUSTRIES LIMITED | `ZUARIIND.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream XTRANET 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-2611-2630-Historical-Data/main/XTRANET/1m/2026/10/XTRANET_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
