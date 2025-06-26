# 🧬 DEG Analysis Pipeline

> A modular and reproducible RNA-seq analysis pipeline built in Python for identifying differentially expressed genes (DEGs), performing enrichment analysis, and generating ready-to-publish visual reports.

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://python.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Jupyter](https://img.shields.io/badge/Jupyter-Compatible-orange.svg)](https://jupyter.org)
[![Colab](https://img.shields.io/badge/Google%20Colab-Ready-brightgreen.svg)](https://colab.research.google.com)

Designed for researchers, students, and bioinformaticians interested in transcriptomic data exploration and portfolio-ready reporting.

## ⚠️ Important Notice

> **This pipeline is intended for academic and research purposes only.**  
> While results may be biologically meaningful, they require proper experimental validation.  
> Use responsibly, cite appropriately, and refer to license terms below for reuse.

## ✨ Features

- 📈 **DEG Analysis** - Welch's t-test with FDR correction for robust statistical analysis
- 🔬 **Functional Enrichment** - GSEA using `gseapy` with Enrichr databases (GO, KEGG)
- 🎯 **Smart Filtering** - Threshold-based filtering of significant genes
- 📊 **Rich Visualizations** - Volcano plots, heatmaps, and enrichment summaries
- 📁 **Comprehensive Export** - DEGs, expression matrices, metadata, and Excel summaries
- 📝 **Auto-generated Reports** - Markdown reports ready for publication or portfolios
- 🔧 **Platform Flexible** - Full compatibility with Google Colab and Jupyter notebooks

## 🚀 Quick Start

### Prerequisites

```bash
# Required Python packages
pip install pandas numpy scipy matplotlib seaborn gseapy openpyxl
```

### Basic Usage

```python
# Clone the repository
git clone https://github.com/engkinandatama/deg-analysis-pipeline.git
cd deg-analysis-pipeline

# Run the analysis (example)
python deg_analysis.py --input your_expression_data.csv --metadata sample_metadata.csv
```

### Google Colab

```python
# Install dependencies in Colab
!pip install gseapy openpyxl

# Upload your data files and run the pipeline
# Detailed instructions in the notebook
```

## 📁 Output Structure

The pipeline generates a comprehensive output directory with all results organized:

```
📂 DEG_analysis_YYYYMMDD_HHMMSS/
├── 📄 PROJECT_REPORT.md                    # Auto-generated summary report
├── 📊 DEG_analysis_complete.xlsx           # All results in Excel format
├── 📂 GSEA_results/
│   ├── KEGG_2021_Human_enrichment.tsv     # KEGG pathway enrichment
│   └── GO_Biological_Process_2023_enrichment.tsv  # GO term enrichment
├── 📋 gene_lists_all_significant.txt       # List of significant genes
├── 📈 ranked_gene_list.rnk                # Ranked gene list for GSEA
└── 📂 plots/
    ├── 01_volcano_plot.png                # Volcano plot visualization
    ├── 02_heatmap_top_genes.png           # Heatmap of top DEGs
    └── 07_enrichment_summary.png          # Enrichment analysis summary
```

## 📖 Documentation

### Input Requirements

- **Expression Data**: CSV file with genes as rows and samples as columns
- **Metadata**: CSV file with sample information and group assignments
- **Format**: Standard RNA-seq count data or normalized expression values

### Key Parameters

- **Log2 Fold Change Threshold**: Default ±1.0
- **P-value Cutoff**: Default 0.05 (FDR corrected)
- **Enrichment Databases**: GO Biological Process, KEGG Pathways
- **Visualization**: Customizable color schemes and themes

## 🔬 Methods

The pipeline implements established bioinformatics methods:

1. **Statistical Testing**: Welch's t-test for unequal variances
2. **Multiple Testing Correction**: Benjamini-Hochberg FDR
3. **Enrichment Analysis**: Gene Set Enrichment Analysis (GSEA)
4. **Visualization**: Publication-ready plots with customizable aesthetics

## 🤝 Contributing

Contributions are welcome! Please feel free to submit issues, feature requests, or pull requests.

### Development Setup

```bash
git clone https://github.com/engkinandatama/deg-analysis-pipeline.git
cd deg-analysis-pipeline
pip install -r requirements.txt
```

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

**You are free to:**
- ✅ Use commercially
- ✅ Modify and distribute
- ✅ Use privately
- ✅ Sublicense

**Attribution is appreciated but not required.**

## 📚 Citation

If this pipeline helps your research or portfolio, please consider citing:

```bibtex
@software{nandatama2025deg,
  author = {Nandatama, Engki},
  title = {DEG Analysis Pipeline in Python},
  year = {2025},
  url = {https://github.com/engkinandatama/deg-analysis-pipeline}
}
```

### Core Dependencies

Please also cite the core libraries that make this pipeline possible:

- **GSEApy**: Fang et al., Bioinformatics, 2021 - [GSEApy GitHub](https://github.com/zqfang/GSEApy)
- **MyGene.info**: BioThings API - [MyGene.info](https://mygene.info)

## ⚠️ Disclaimer

- This analysis is designed for **educational and exploratory research only**
- Biological findings should be validated through appropriate wet-lab experiments
- **Do not use for clinical diagnostics or treatment decisions**
- Results require proper experimental validation before publication

## 👨‍🔬 Author

**Engki Nandatama**  
🧪 *Code-driven biologist*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue.svg)](https://linkedin.com/in/engkinandatama)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black.svg)](https://github.com/engkinandatama)

---

**Feel free to fork, adapt, or contribute to this project for your own research endeavors. Happy transcriptome exploring! 🧬✨**
