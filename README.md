## 本範本與原始來源的差異（SWPM Workshop 用）

本 repo 為 SWPM Workshop 的教學範本，fork 自 [coffeefuelbump/csv-data-summarizer-claude-skill](https://github.com/coffeefuelbump/csv-data-summarizer-claude-skill)。與原始來源的差異只有以下兩項：

- 技能位置搬移：`SKILL.md`、`analyze.py`、`requirements.txt`、`resources/` 搬到 Claude Code 專案技能位置 `.claude/skills/csv-data-summarizer/`，檔案內容不變。下方上游原文中「What's Included」的目錄樹與安裝指令（`pip install -r requirements.txt`）仍以搬移前的根目錄為準，與本 repo 不符，需加上 `.claude/skills/csv-data-summarizer/` 前綴；`SKILL.md`、`resources/README.md`、`analyze.py` 內的相對路徑是相對於技能資料夾寫的，在 `.claude/skills/csv-data-summarizer/` 內執行時仍然成立。上游原文依規則不修改。
- 新增 `data/`：放清洗後的筆電規格資料 `data/laptops.csv`，來源、授權與修改說明見 `data/README.md`。

授權：上游 README 聲明採 MIT 授權（原 repo 無 LICENSE 檔）；本 repo 的修改同樣以 MIT 提供；`data/` 內資料依原上傳者標示為 Apache-2.0，授權全文見 `data/LICENSE-Apache-2.0.txt`。

公開資料集，僅供演練。

---
<div align="center">

[![Join AI Community](https://img.shields.io/badge/🚀_Join-AI_Community_(FREE)-4F46E5?style=for-the-badge)](https://www.skool.com/ai-for-your-business)
[![GitHub Profile](https://img.shields.io/badge/GitHub-@coffeefuelbump-181717?style=for-the-badge&logo=github)](https://github.com/coffeefuelbump)

[![Link Tree](https://img.shields.io/badge/Linktree-Everything-green?style=for-the-badge&logo=linktree&logoColor=white)](https://linktr.ee/corbin_brown)
[![YouTube Membership](https://img.shields.io/badge/YouTube-Become%20a%20Builder-red?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/channel/UCJFMlSxcvlZg5yZUYJT0Pug/join)

</div>

---

# 📊 CSV Data Summarizer - Claude Skill

A powerful Claude Skill that automatically analyzes CSV files and generates comprehensive insights with visualizations. Upload any CSV and get instant, intelligent analysis without being asked what you want!

<div align="center">

[![Version](https://img.shields.io/badge/version-2.1.0-blue.svg)](https://github.com/coffeefuelbump/csv-data-summarizer-claude-skill)
[![Python](https://img.shields.io/badge/python-3.8+-green.svg)](https://www.python.org/)
[![License](https://img.shields.io/badge/license-MIT-orange.svg)](LICENSE)

</div>

## 🚀 Features

- **🤖 Intelligent & Adaptive** - Automatically detects data type (sales, customer, financial, survey, etc.) and applies relevant analysis
- **📈 Comprehensive Analysis** - Generates statistics, correlations, distributions, and trends
- **🎨 Auto Visualizations** - Creates multiple charts based on what's in your data:
  - Time-series plots for date-based data
  - Correlation heatmaps for numeric relationships
  - Distribution histograms
  - Categorical breakdowns
- **⚡ Proactive** - No questions asked! Just upload CSV and get complete analysis immediately
- **🔍 Data Quality Checks** - Automatically detects and reports missing values
- **📊 Multi-Industry Support** - Adapts to e-commerce, healthcare, finance, operations, surveys, and more

## 📥 Quick Download

<div align="center">

### Get Started in 2 Steps

**1️⃣ Download the Skill**  
[![Download Skill](https://img.shields.io/badge/Download-CSV%20Data%20Summarizer%20Skill-blue?style=for-the-badge&logo=download)](https://github.com/coffeefuelbump/csv-data-summarizer-claude-skill/raw/main/csv-data-summarizer.zip)

**2️⃣ Try the Demo Data**  
[![Download Demo CSV](https://img.shields.io/badge/Download-Sample%20P%26L%20Financial%20Data-green?style=for-the-badge&logo=data)](https://github.com/coffeefuelbump/csv-data-summarizer-claude-skill/raw/main/examples/showcase_financial_pl_data.csv)

</div>

---

## 📦 What's Included

```
csv-data-summarizer-claude-skill/
├── SKILL.md              # Claude Skill definition
├── analyze.py            # Comprehensive analysis engine
├── requirements.txt      # Python dependencies
├── examples/
│   └── showcase_financial_pl_data.csv  # Demo P&L financial dataset (15 months, 25 metrics)
└── resources/
    ├── sample.csv        # Example dataset
    └── README.md         # Usage documentation
```

## 🎯 How It Works

1. **Upload** any CSV file to Claude.ai
2. **Skill activates** automatically when CSV is detected
3. **Analysis runs** immediately - inspects data structure and adapts
4. **Results delivered** - Complete analysis with multiple visualizations

No prompting needed. No options to choose. Just instant, comprehensive insights!

## 📥 Installation

### For Claude.ai Users

1. Download the latest release: [`csv-data-summarizer.zip`](https://github.com/coffeefuelbump/csv-data-summarizer-claude-skill/releases)
2. Go to [Claude.ai](https://claude.ai) → Settings → Capabilities → Skills
3. Upload the zip file
4. Enable the skill
5. Done! Upload any CSV and watch it work ✨

### For Developers

```bash
git clone git@github.com:coffeefuelbump/csv-data-summarizer-claude-skill.git
cd csv-data-summarizer-claude-skill
pip install -r requirements.txt
```

## 📊 Sample Dataset Highlights

The included demo CSV contains **15 months of P&L data** with:
- 3 product lines (SaaS, Enterprise, Services)
- 25 financial metrics including revenue, expenses, margins, CAC, LTV
- Quarterly trends showing business growth
- Perfect for showcasing time-series analysis, correlations, and financial insights

## 🎨 Example Use Cases

- **📊 Sales Data** → Revenue trends, product performance, regional analysis
- **👥 Customer Data** → Demographics, segmentation, geographic patterns
- **💰 Financial Data** → Transaction analysis, trend detection, correlations
- **⚙️ Operational Data** → Performance metrics, time-series analysis
- **📋 Survey Data** → Response distributions, cross-tabulations

## 🛠️ Technical Details

**Dependencies:**
- Python 3.8+
- pandas 2.0+
- matplotlib 3.7+
- seaborn 0.12+

**Visualizations Generated:**
- Time-series trend plots
- Correlation heatmaps
- Distribution histograms
- Categorical bar charts

## 📝 Example Output

```
============================================================
📊 DATA OVERVIEW
============================================================
Rows: 100 | Columns: 15

📋 DATA TYPES:
  • order_date: object
  • total_revenue: float64
  • customer_segment: object
  ...

🔍 DATA QUALITY:
✓ No missing values - dataset is complete!

📈 NUMERICAL ANALYSIS:
[Summary statistics for all numeric columns]

🔗 CORRELATIONS:
[Correlation matrix showing relationships]

📅 TIME SERIES ANALYSIS:
Date range: 2024-01-05 to 2024-04-11
Span: 97 days

📊 VISUALIZATIONS CREATED:
  ✓ correlation_heatmap.png
  ✓ time_series_analysis.png
  ✓ distributions.png
  ✓ categorical_distributions.png
```

## 🌟 Connect & Learn More

<div align="center">

[![Join AI Community](https://img.shields.io/badge/Join-AI%20Community%20(FREE)-blue?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0IiBmaWxsPSJ3aGl0ZSI+PHBhdGggZD0iTTEyIDJDNi40OCAyIDIgNi40OCAyIDEyczQuNDggMTAgMTAgMTAgMTAtNC40OCAxMC0xMFMxNy41MiAyIDEyIDJ6bTAgM2MxLjY2IDAgMyAxLjM0IDMgM3MtMS4zNCAzLTMgMy0zLTEuMzQtMy0zIDEuMzQtMyAzLTN6bTAgMTQuMmMtMi41IDAtNC43MS0xLjI4LTYtMy4yMi4wMy0xLjk5IDQtMy4wOCA2LTMuMDggMS45OSAwIDUuOTcgMS4wOSA2IDMuMDgtMS4yOSAxLjk0LTMuNSAzLjIyLTYgMy4yMnoiLz48L3N2Zz4=)](https://www.skool.com/ai-for-your-business/about)

[![Link Tree](https://img.shields.io/badge/Linktree-Everything-green?style=for-the-badge&logo=linktree&logoColor=white)](https://linktr.ee/corbin_brown)

[![YouTube Membership](https://img.shields.io/badge/YouTube-Become%20a%20Builder-red?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/channel/UCJFMlSxcvlZg5yZUYJT0Pug/join)

[![Twitter Follow](https://img.shields.io/badge/Twitter-Follow%20@corbin__braun-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/corbin_braun)

</div>

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests
- Share your use cases

## 📄 License

MIT License - feel free to use this skill for personal or commercial projects!

## 🙏 Acknowledgments

Built for the Claude Skills platform by [Anthropic](https://www.anthropic.com/news/skills).

---

<div align="center">

**Made with ❤️ for the AI community**

⭐ Star this repo if you find it useful!

</div>

