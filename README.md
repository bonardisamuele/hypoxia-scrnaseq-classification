# Hypoxia classification from single-cell RNA-seq

**Academic team project | 2026 | Python**

Can hypoxic and normoxic cancer cells be distinguished from single-cell gene-expression profiles, and how does that signal transfer between cell lines and sequencing technologies? This project studies HCC1806 and MCF7 breast cancer cell lines using course-supplied SmartSeq and DropSeq expression matrices and metadata.

## Authors and contributions

**Samuele Bonardi, Lorenzo Mossini, Mattia Gasparetto, Dario Bonati and Riccardo Torriero.** This is the complete, group-approved notebook. Samuele's principal contribution was supervised learning and the subsequent sections: classifier comparison, tuning, stacking, evaluation, cross-cell-line/cross-technology transfer and pathway analysis. Earlier exploratory, quality-control, preprocessing and unsupervised sections belong to the team workflow and are not individually attributed to him.

## Workflow

The analysis covers exploratory data analysis, sparsity and quality control, normalisation, PCA, clustering and NMF; supervised baselines and classifiers with feature-selection/preprocessing pipelines; stacking and evaluation diagnostics; transfer between cell lines and technologies; and gene-set/pathway interpretation with ORA/GSEA. It ends with unlabelled-sample predictions and conclusions.

## Where to start

- [Complete notebook](notebooks/hypoxia_classification.ipynb): all **316 original scientific cells**, including **158 code cells**. Read the problem/EDA sections for context, then supervised learning, stacking, transfer and pathway sections for Samuele's main work.
- [Dependency inventory](environment/requirements.in): unpinned distributions inferred from imports, including NumPy, pandas, scikit-learn, scanpy/anndata, XGBoost, Optuna and gseapy. This is not a validated environment lockfile.

Saved notebook outputs and execution metadata have been cleared. The source narrative and calculations are preserved; this copy does not display the previous execution's plots or scores. No new numerical accuracy or biomarker claim is made here.

## Data and reproduction limits

Expression matrices, cell annotations and derived CSV files are not bundled. The notebook starts from `PROJECT_DIR = Path(".")`, expects SmartSeq/QCd inputs under that directory and DropSeq inputs under `DropSeq/`, and also references derived files. Reproduction requires authorised versions of all those inputs and an explicitly chosen working directory. The notebook records the original input assumptions; no replacement data is manufactured.

No complete execution, environment installation, model tuning or enrichment request was performed for this release. Some enrichment routines can contact external services. Internal stratified cross-validation, held-out cell evaluation and transfer experiments answer different questions; they do not establish patient-level independence, clinical utility or causal biomarkers. Static source checks are not a complete leakage assessment or numerical replication.

## Reuse

No software licence has been selected for this repository. Public access alone does not grant an unrestricted reuse licence; dataset and third-party terms remain separate.
