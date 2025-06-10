# env-setup
A repository to store standardized workflow setup for data science and bioinformatics projects

## Essential Packages for Data Analysis 
```R
# 📌 Core packages for data wrangling and visualization
install.packages(c(
  "tidyverse",     # Includes dplyr, ggplot2, readr, tibble, etc.
  "readxl",        # Read Excel files
  "janitor",       # Clean column names and tables
  "skimr",         # Quick data summaries
  "here",          # File path management
  "tidyplots"      # Generate publication-ready plots for scientific papers
  "patchwork",     # Combine ggplots
  "plotly"         # Interactive plots
))
```
```R
# 📊 Table and summary reporting
install.packages(c(
  "gtsummary",     # Summary tables for clinical-style reports
  "gt"             # Table formatting engine used by gtsummary
))
```

```R
# 🧠 Easystats ecosystem (modeling, diagnostics, interpretation)
install.packages("easystats")  # Meta-package that includes:
# - insight
# - parameters
# - performance
# - report
# - effectsize
# - bayestestR
# - see
# - modelbased
```

```R
# ✅ Optional (recommended for statistical modeling workflows)
install.packages(c(
  "broom",         # Tidy up model outputs
  "car",           # Companion to Applied Regression
  "MASS"           # Core statistical functions and data
))
```

## 🧬 Bulk RNA-seq Analysis Package Installation
```R
# 📌 Install Bioconductor manager if not already available
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")

# 📦 Core differential expression packages
BiocManager::install(c(
  "DESeq2",         # Differential expression via negative binomial
  "edgeR",          # Differential expression using empirical Bayes
  "limma",          # Linear modeling and voom transformation
  "apeglm"          # Shrinkage estimator for log fold changes (used with DESeq2)
))

# 📥 Transcript/Gene-level data import
BiocManager::install(c(
  "tximport",       # Import transcript-level quantifications
  "tximeta"         # Extension of tximport with metadata tracking
))

# 🧬 Annotation and metadata
BiocManager::install(c(
  "biomaRt",        # Interface to Ensembl biomart databases
  "AnnotationDbi",  # Base class for annotation packages
  "org.Hs.eg.db",   # Human gene annotation (use org.Mm.eg.db for mouse, etc.)
  "GenomicFeatures",# Generate TxDb objects
  "ensembldb"       # Manage Ensembl-based annotations
))

# 📊 Visualization and summary
BiocManager::install(c(
  "pheatmap",         # Heatmaps
  "ComplexHeatmap",   # Advanced heatmaps
  "EnhancedVolcano",  # Volcano plots for DE results
))

# 📈 Functional analysis
BiocManager::install(c(
  "clusterProfiler",  # Enrichment and pathway analysis
  "pathview",         # KEGG pathway mapping
  "fgsea",            # Fast GSEA
  "GSEABase",         # Base support for GSEA
  "GSVA"              # Gene set variation analysis
))

# 🧪 Batch correction and quality control
BiocManager::install(c(
  "sva",              # Surrogate variable analysis for batch effect removal
  "arrayQualityMetrics" # Quality control reports
))
```
## 🧪 Single-Cell RNA-seq Analysis – Package Installation
```R
# 📌 Install Bioconductor manager if needed
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")

# 🧱 Core single-cell infrastructure
BiocManager::install(c(
  "SingleCellExperiment",   # Core data container
  "scater",                 # QC and visualization
  "scran",                  # Normalization
  "scuttle",                # Utilities for scRNA-seq
  "DropletUtils"            # Empty droplet detection for 10x
))

# 🔬 DE and Pseudobulk analysis
BiocManager::install(c(
  "DESeq2",                 # Pseudobulk DE analysis
  "edgeR", "limma",         # Additional DE tools
  "MAST"                    # Single-cell DE
))

# 🧠 Annotation & reference data
BiocManager::install(c(
  "biomaRt", "AnnotationDbi", "org.Hs.eg.db",  # Annotation
  "SingleR", "celldex"                         # Cell type annotation
))

# 🔁 Batch correction & integration
BiocManager::install(c(
  "batchelor",    # FastMNN batch correction
  "harmony"       # Harmony integration (can use with Seurat)
))

# 📊 Dimensionality reduction & visualization
BiocManager::install(c(
  "uwot",         # UMAP
  "Rtsne",        # t-SNE
  "ComplexHeatmap",
  "pheatmap",
  "RColorBrewer"
))

# 🚀 Trajectory inference
BiocManager::install(c(
  "monocle3", "slingshot"
))

# 📥 File format & conversion
BiocManager::install(c(
  "zellkonverter",  # For HDF5 and AnnData interop
  "scRNAseq"        # Benchmark single-cell datasets
))

# 🧪 Install Seurat (CRAN)
install.packages("Seurat")

# 🧠 Optional: Bridge to Python tools like Scanpy
install.packages("reticulate")
```







