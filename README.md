# miRNACancerClassification


This Github Repo includes Random Forest and XGBoost Models that we developed, trained, and optimized. Written in RStudio and developed using the R programming language. <br>

It also includes models' binary classification results and datasets of six cancers:

BRCA.txt <br>
HNSC.txt <br>
KIRC.txt <br>
LIHC.txt <br>
LUAD.txt <br>
THCA.txt <br>
full_BRCA_miR_data.txt 

 **2nd Place - IEEE-SEM Conference** |  **Published in PGHR Johns Hopkins Journal**

This research project applies supervised machine learning to classify breast cancer tumor vs. control samples using microRNA (miRNA) expression data. By identifying statistically significant miRNA biomarkers, the models achieve high accuracy in distinguishing cancerous from healthy tissue.

**Research conducted as part of UMich R Camp (July - October 2022)**

## Features

- **Rigorous Feature Selection**: Statistical filtering using t-tests (p < 0.001) reduced 1000+ miRNAs to 58 highly significant biomarkers
- **Dual ML Approach**: Implemented both Random Forest and XGBoost classifiers for robust comparison
- **High Performance**: Achieved strong classification accuracy on held-out test data
- **Reproducible Pipeline**: Complete data preprocessing, training, and evaluation workflow

## Dataset

- **Source**: BRCA (Breast Cancer) miRNA expression data
- **Samples**: 172 total (86 tumor, 86 control)
- **Features**: 58 statistically significant miRNAs (after selection from full dataset)
- **Split**: 80/20 train-test ratio with stratified sampling

## Results


-  Models successfully distinguish tumor from control samples
-  58 miRNA biomarkers identified with statistical significance

## Installation & Usage

### Prerequisites
```r
# Install required packages
install.packages("randomForest")
install.packages("xgboost")
```

### Running the Analysis
```r
# Set working directory
setwd("path/to/project")

# Load data
brca_miR_data <- read.table("Full_BRCA_miR_data.txt", 
                            header = T, 
                            row.names = 1, 
                            stringsAsFactors = F)

# Run analysis (see full code in randomforest.Rmd)
source("randomforest.R")
```


## Biological Significance

MicroRNAs are small non-coding RNA molecules that regulate gene expression and play crucial roles in cancer development. This project demonstrates:

- miRNAs can serve as effective biomarkers for cancer detection
- Machine learning can identify complex patterns in high-dimensional biological data
- Statistical rigor in feature selection prevents overfitting
- Potential for clinical diagnostic applications

## Technologies
```
R (v4.0+)
├── randomForest (classification)
├── xgboost (gradient boosting)
└── base R (statistical testing, data manipulation)
```

## Citation
```bibtex
@article{huang2022mirna,
  title={miRNA-Based Cancer Classification using Machine Learning},
  author={Huang, Julia},
  journal={PGHR Johns Hopkins Journal},
  year={2022},
  note={2nd Place, IEEE-SEM Conference}
}
```

## Acknowledgments

- **UMich R Camp Research Program** for project mentorship
- **IEEE-SEM Conference** for presentation platform
- **PGHR Johns Hopkins** for publication opportunity
