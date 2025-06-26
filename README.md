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
# Core required packages
pip install pandas numpy scipy matplotlib seaborn statsmodels

# Optional but recommended (for GSEA analysis)
pip install gseapy mygene openpyxl
```

### Option 1: Python Script (DEG.py)

```python
# Clone the repository
git clone https://github.com/engkinandatama/deg-analysis-pipeline.git
cd deg-analysis-pipeline

# Run the Python script
python DEG.py

# Follow the interactive prompts to:
# 1. Upload your expression data (tsv format)
# 2. Upload sample metadata (tsv format)
# 3. Configure analysis parameters
```

### Option 2: Jupyter Notebook (DEG.ipynb)

```python
# Launch Jupyter Notebook
jupyter notebook DEG.ipynb

# Or use Jupyter Lab
jupyter lab DEG.ipynb
```

### Option 3: Google Colab
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/16CbByses6BNWI3Eoe2OpdiE0GjMQ6FL9?usp=sharing)
```python
# Install dependencies in Colab
!pip install gseapy mygene openpyxl

# Upload DEG.ipynb to Google Colab
# Upload your data files when prompted
# Run cells sequentially
```

## 📁 Output Structure

The pipeline generates a comprehensive output directory with all results organized:

```
📂 DEG_analysis_YYYYMMDD_HHMMSS/
├── 📊 Analysis Results
│   ├── 02_DEG_results_complete.tsv        # Complete DEG analysis results
│   ├── 03_DEG_significant_genes.tsv       # Significant genes only
│   ├── 06_heatmap_gene_list.tsv          # Genes used in heatmap
│   └── 09_analysis_summary.txt           # Text summary report
│
├── 📋 Gene Lists
│   ├── gene_lists_all_significant.txt     # All significant genes
│   ├── gene_lists_upregulated.txt        # Upregulated genes only
│   ├── gene_lists_downregulated.txt      # Downregulated genes only
│   └── ranked_gene_list.rnk              # Ranked gene list for GSEA
│
├── 📁 Export Files
│   ├── expression_significant_genes.tsv   # Expression data for significant genes
│   ├── sample_metadata.tsv               # Sample information
│   └── DEG_analysis_complete.xlsx        # Complete results in Excel format
│
├── 📂 GSEA_results/                       # GSEA enrichment analysis
│   ├── KEGG_2021_Human_enrichment.tsv    # KEGG pathway enrichment
│   └── GO_Biological_Process_2023_enrichment.tsv  # GO term enrichment
│
└── 📂 Visualizations
    ├── 01_exploratory_analysis.png       # Initial data exploration
    ├── 04_volcano_plot.png               # Volcano plot visualization
    ├── 05_heatmap_top_genes.png          # Heatmap of top DEGs
    ├── 07_enrichment_summary.png         # GSEA results summary
    └── 08_analysis_summary.png           # Summary plots and metrics
```

## 📖 Documentation

### Pipeline Components

- **DEG.py** - Standalone Python script for automated analysis
- **DEG.ipynb** - Interactive Jupyter notebook with step-by-step guidance

### Input Requirements

- **Expression Data**: tsv file with genes as rows and samples as columns
- **Metadata**: tsv file with sample information and group assignments
- **Format**: Standard RNA-seq count data or normalized expression values

### Pipeline Initialization

The pipeline automatically sets up the analysis environment:

```python
# Automatic setup includes:
# - Import required libraries (pandas, numpy, scipy, matplotlib, seaborn)
# - Check for optional packages (gseapy, mygene)
# - Create timestamped output directory
# - Configure plotting parameters
# - Initialize analysis logging
```

### Key Parameters

- **Log2 Fold Change Threshold**: Default ±1.0
- **P-value Cutoff**: Default 0.05 (FDR corrected)
- **Statistical Test**: Welch's t-test or Mann-Whitney U
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

# Install core dependencies
pip install pandas numpy scipy matplotlib seaborn statsmodels

# Install optional dependencies for full functionality
pip install gseapy mygene openpyxl

# Choose your preferred method:
# 1. Run the Python script: python DEG.py
# 2. Open Jupyter notebook: jupyter notebook DEG.ipynb
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
