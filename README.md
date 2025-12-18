🏎️ F1 Strategy Simulator – Real-World Data-Driven Race Strategy Engine
A real-world inspired Formula 1 race strategy simulator built using historical lap-by-lap data and machine learning models to emulate decision-making similar to an F1 strategy wall.

This project predicts lap times, tyre degradation, pit windows, safety car probability, and undercut potential, and combines them into a unified strategy engine with a Streamlit-based interactive interface.

🎥 Demo:


🎯 Project Objective
To simulate realistic Formula 1 race strategy decisions using:

Historical F1 race data
Machine learning prediction models
Domain-driven feature engineering
A modular, production-style architecture
🧠 Strategy Components Implemented
✔ Lap Time Prediction ✔ Tyre Wear Prediction ✔ Pit Window Prediction ✔ Safety Car Probability Estimation (Approximate) ✔ Undercut Effect Estimation ✔ Unified Strategy Engine

📂 Project Structure
f1_strategy_simulator/
│
├── data/
│   ├── raw/                  # Original Kaggle F1 datasets
│   ├── features/
│   │   └── features_master.csv
│   └── processed/
│       ├── master_lap_by_lap.csv
│       ├── pit_stop_enriched.csv
│       └── stint_aggregates.csv
│
├── models/
│   ├── lap_time_predictor.pkl
│   ├── tyre_wear_predictor.pkl
│   ├── pit_window_model.pkl
│   ├── safety_car_model.pkl
│   └── undercut_model.pkl
│
├── src/
│   ├── data/
│   │   ├── load_data.py
│   │   ├── preprocess.py
│   │   └── feature_engineering.py
│   │
│   ├── models/
│   │   ├── lap_time_model.py
│   │   ├── tyre_wear_model.py
│   │   ├── pit_window_model.py
│   │   ├── safety_car_model.py
│   │   └── undercut_model.py
│   │
│   ├── simulator/
│   │   └── strategy_engine.py
│   │
│   └── app/
│       └── streamlit_app.py
│
├── requirements.txt
└── README.md
🔍 Model Overview
Model	Purpose
Lap Time Predictor	Predicts next-lap lap time
Tyre Wear Predictor	Estimates tyre degradation per stint
Pit Window Model	Identifies optimal pit laps
Safety Car Model	Estimates safety car probability (approximate, data-driven)
Undercut Model	Estimates undercut advantage using pit delta and tyre age
⚙️ Strategy Engine Logic
The strategy_engine.py combines model outputs to:

Compare stay-out vs pit scenarios
Quantify undercut advantage
Adjust decisions based on tyre age & safety car risk
Recommend optimal pit timing
This mirrors real F1 race strategy evaluation logic.

🖥️ Streamlit Application
The Streamlit UI allows:

Interactive driver & stint selection
Strategy recommendations
Visualization of predicted lap times & pit effects
Run locally:

streamlit run src/app/streamlit_app.py
📊 Dataset
Source: Kaggle Formula 1 World Championship datasets
Granularity: Lap-by-lap
Time range: Multiple seasons
Enriched with pit stop and stint-level features
--

⚠ Disclaimer
It is an educational and analytical project inspired by publicly available data.
