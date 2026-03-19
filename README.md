# B-READY 2025 Data Explorer

An interactive, single-file HTML dashboard for exploring the World Bank **Business Ready (B-READY) 2025** dataset — covering **101 economies**, **10 topics**, and **3 pillars** of business environment assessment.

> **[Launch Dashboard →](https://jsrinivasan1.github.io/B-READY-2025-Data-Explorer/)**

---

## Overview

The B-READY (Business Ready) project is the World Bank's flagship benchmarking initiative measuring the business and investment climate across economies worldwide. It replaced the former Doing Business report with a broader, more balanced methodology organized around three pillars:

| Pillar | Focus |
|--------|-------|
| **Pillar 1** | Regulatory Framework — quality and adequacy of business regulations |
| **Pillar 2** | Public Services — efficiency and accessibility of government services |
| **Pillar 3** | Operational Efficiency — ease and cost of regulatory compliance in practice |

These pillars are assessed across **10 topics**: Business Entry, Business Location, Utility Services, Labor, Financial Services, International Trade, Taxation, Dispute Resolution, Market Competition, and Business Insolvency.

This dashboard makes the full B-READY 2025 dataset interactive and explorable — no installation or server required.

---

## Features

### 📊 Overview Tab
- Summary statistics across all 101 economies
- Average pillar scores by **income group** (HIC / UMIC / LMIC / LIC) and **World Bank region**
- Topic score distributions (25th percentile, median, 75th percentile)
- Pillar balance scatter plot — weakest vs. strongest pillar per economy

### 🏆 Rankings Tab
- Full sortable economy rankings
- Filter by **region**, **income group**, or **topic**
- Rank by overall average or any individual pillar
- Visual score bars for quick comparison

### 🔍 Economy Profile Tab
- Searchable dropdown with all 101 economies (click to open, type to filter)
- Radar chart showing pillar scores across all 10 topics
- Horizontal bar chart of topic-level overall scores (color-coded by performance tier)
- Detailed pillar breakdown with animated progress bars for each topic

### ⚖️ Compare Tab
- Side-by-side comparison of up to **6 economies**
- Searchable dropdown (already-selected economies are excluded)
- Overlay radar chart and grouped bar chart
- Full comparison table covering all metrics

### 📈 Scatter Analysis Tab
- **44 selectable variables** for X and Y axes — any combination of pillar scores, topic overalls, and topic-pillar breakdowns
- Color-code points by **income group** or **region**
- Toggle economy labels: all, outliers only, or none
- Auto-computed **Pearson correlation (r)**, **R²**, **slope**, and **trend line**

---

## Data

All data is embedded directly in the HTML file — no external API calls or data files required.

**Source:** [World Bank B-READY 2025](https://www.worldbank.org/en/businessready)

The dataset includes:
- **101 economies** with full pillar and topic scores
- **3 pillars** × **10 topics** = 30 pillar-topic combinations per economy
- Category-level breakdowns within each topic
- Economy metadata: ISO 3-letter code, World Bank region, income classification

---

## Usage

### Option 1: Open directly
Download `index.html` and open it in any modern browser. Everything is self-contained.

### Option 2: GitHub Pages
This repo is configured for GitHub Pages. The dashboard is live at the URL above.

### Option 3: Local server
```bash
# Any simple HTTP server works
python -m http.server 8000
# Then open http://localhost:8000
```

---

## Technical Notes

- **Zero dependencies at runtime** — only Chart.js (loaded from CDN) and Google Fonts
- **Single HTML file** (~425 KB) with embedded data, styles, and scripts
- Works offline once loaded (except for the CDN font/chart library on first load)
- Responsive layout adapts to tablet and mobile screens
- Keyboard navigation supported in economy search dropdowns (arrow keys + enter)

---

## Color Conventions

Follows World Bank B-READY visual standards:

| Element | Color |
|---------|-------|
| Pillar 1 (Regulatory) | `#5B9BD5` blue |
| Pillar 2 (Public Services) | `#FFC000` gold |
| Pillar 3 (Efficiency) | `#70AD47` green |
| High income | `#2E75B6` |
| Upper middle income | `#70AD47` |
| Lower middle income | `#ED7D31` |
| Low income | `#FFC000` |

---

## License

The underlying data is published by the World Bank under its [open data terms](https://www.worldbank.org/en/about/legal/terms-of-use-for-datasets). This dashboard visualization is provided as-is for research and educational use.

---

## Citation

World Bank. 2025. *Business Ready 2025.* Washington, DC: World Bank.
