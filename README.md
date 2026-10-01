## 🛠 Project Architecture

```text
entity-resolution-pipeline/
│
├── data/                            # Dataset directory (git-ignored)
│   ├── raw/                         # Raw entity source files (.tsv)
│   ├── candidates/                  # Extracted candidate pairs (.tsv)
│   └── features/                    # Computed pairwise features (.parquet)
│
├── src/                             # Pipeline modules
│   ├── __init__.py
│   ├── candidate_gen.py             # Candidate generation & pruning
│   ├── feature_extraction.py        # Polars & RapidFuzz feature logic
│   ├── train.py                     # LightGBM model training & tuning
│   └── predict.py                   # Checkpoint inference & submission generator
│
├── models/                          # Model checkpoints (git-ignored)
│   └── lgbm_model.txt
│
├── output/                          # Execution outputs
│   └── matching_results.tsv
│
├── .gitignore                       # Git exclusions for large datasets
├── requirements.txt                 # Python dependencies
├── main.py                          # Pipeline orchestrator
└── README.md                        # Project documentation
