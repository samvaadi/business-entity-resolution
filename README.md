entity-resolution-pipeline/
│
├── data/                      # Local testing directory (git-ignored)
│   ├── raw/                   # Raw source entity files
│   ├── candidates/            # Generated candidate pairs
│   └── features/              # Parquet feature matrices
│
├── src/                       # core pipeline package
│   ├── __init__.py
│   ├── candidate_gen.py       # Teammate's candidate generation logic
│   ├── feature_extraction.py  # RapidFuzz & Polars feature engineering
│   ├── train.py               # LightGBM training & F0.5 calibration
│   └── predict.py             # Checkpoint inference & submission output
│
├── models/                    # Model artifacts (git-ignored)
│   └── lgbm_model.txt
│
├── .gitignore
├── requirements.txt           # Environment dependencies
├── main.py                    # Orchestrator (runs full pipeline)
└── README.md                  # Setup & usage instructions

//tentative pipeline structure
