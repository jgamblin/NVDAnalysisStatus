# NVD CVE Analysis Status Tracker

[![Update Report](https://github.com/jgamblin/NVDAnalysisStatus/actions/workflows/UpdateReport.yml/badge.svg)](https://github.com/jgamblin/NVDAnalysisStatus/actions/workflows/UpdateReport.yml)

An automated tracker monitoring the National Vulnerability Database (NVD) CVE analysis backlog since February 15, 2024 — the date NIST [announced reduced capacity](https://nvd.nist.gov/general/news/nvd-program-transition-announcement) for CVE enrichment and analysis.

## 📊 What This Tracks

On February 15, 2024, NVD announced they would be reducing their CVE analysis efforts, creating a growing backlog of unanalyzed vulnerabilities. This project provides:

- **Total CVEs published** since the announcement
- **Complete status breakdown** of all CVE states (Analyzed, Awaiting Analysis, Undergoing Analysis, Modified, Rejected, Received)
- **Backlog metrics** showing work remaining and estimated days to clear
- **Calendar heatmaps** visualizing daily analysis and publication rates

## 🔄 Auto-Updated Every 6 Hours

Data is automatically refreshed via GitHub Actions, pulling the latest CVE data from the NVD. 

## 📈 View the Report

Open **[NVDVulnStatus.ipynb](NVDVulnStatus.ipynb)** to see the latest analysis with interactive charts and statistics.

## 🛠️ Local Setup

```bash
# Clone the repo
git clone https://github.com/jgamblin/NVDAnalysisStatus.git
cd NVDAnalysisStatus

# Install dependencies
pip install -r requirements.txt

# Download latest NVD data
wget https://nvd.handsonhacking.org/nvd.jsonl

# Run the notebook
jupyter notebook NVDVulnStatus.ipynb
```

## 📋 CVE Status Definitions

| Status | Description |
|--------|-------------|
| **Analyzed** | CVE has been fully analyzed with CVSS scores and CPE data |
| **Awaiting Analysis** | CVE is in the queue waiting to be analyzed |
| **Undergoing Analysis** | CVE is currently being processed by NVD analysts |
| **Modified** | CVE was analyzed but has been modified and needs re-analysis |
| **Rejected** | CVE was rejected (duplicate, disputed, or invalid) |
| **Received** | CVE was just received and not yet queued for analysis |

## 📜 License

[MIT](LICENSE)

## 🙏 Acknowledgments

- NVD data sourced from [nvd.handsonhacking.org](https://nvd.handsonhacking.org/)
- Original NVD data from [NIST NVD](https://nvd.nist.gov/)
