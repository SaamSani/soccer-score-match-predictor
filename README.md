
# ⚽ Soccer Score and Match Outcome Predictor

This project is an end-to-end machine learning system that predicts the **outcome** (Win/Draw/Loss) and **final score** of professional soccer matches. It uses team strength, recent form, and head-to-head matchup history. The model was trained on 85,000+ matches from 2008–2025 using real-world data.

---

## 🔧 Project Structure

```
soccer-score-match-predictor/
├── data/                   # ⚠️ Empty — add raw data here (see below)
│   ├── football.json-master/
│   └── champions-league-master/
│
├── models/                 # ⚠️ Populated after training models
│   ├── rf_model_final.joblib
│   ├── home_goal_model_final.joblib
│   └── away_goal_model_final.joblib
│
├── Phase1.ipynb            # Clean and parse raw datasets
├── Phase2.ipynb            # Feature engineering (strength, recent form)
├── Phase3.ipynb            # Train & save prediction models
├── Phase4Final.ipynb       # Live prediction on custom match input
├── .gitignore
└── README.md
```

---

## 📥 Setup Instructions

1. **Clone this repository**  
   ```bash
   git clone https://github.com/SaamSani/soccer-score-match-predictor.git
   cd soccer-score-match-predictor
   ```

2. **Download Required Datasets**
   Download and unzip the following repositories from [openfootball](https://github.com/openfootball):

   - [football.json](https://github.com/openfootball/football.json)
   - [champions-league](https://github.com/openfootball/champions-league)

   Then place them like this:
   ```
   data/
   ├── football.json-master/
   └── champions-league-master/
   ```

3. **Install Dependencies**
   Make sure Python ≥ 3.8 is installed, then run:
   ```bash
   pip install pandas numpy scikit-learn joblib
   ```

4. **Run the Notebooks (in order)**
   - `Phase1.ipynb`: Cleans and merges raw data
   - `Phase2.ipynb`: Generates all match features
   - `Phase3.ipynb`: Trains and saves the models in `models/`
   - `Phase4Final.ipynb`: Allows predictions for future matches via input

---

## 🧠 Models Used

| Task               | Model                  |
|--------------------|------------------------|
| Match Outcome      | Random Forest Classifier |
| Home Goal Prediction | Linear Regression     |
| Away Goal Prediction | Linear Regression     |

---

## ✅ Example Prediction

```
Match: Real Madrid vs Bayern Munich
Predicted Outcome: Draw
Predicted Score: 2 - 2
```

---

## 📌 Notes

- The `data/` and `models/` folders are empty by default.
- They are automatically populated after following setup and running the notebooks.
- The full dataset includes 85,768 matches from 2008 to 2025.

---

## 📬 Contact

Created by [Saam Sani](https://github.com/SaamSani)  
For questions or contributions, please open an issue or connect via [LinkedIn](https://linkedin.com/in/SaamSani).
