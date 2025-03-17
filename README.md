# March-Machine-Learning-Mania-2025
This is a documentation for one of my submissions for Kaggle's annual machine learning competition sponsored by Google. (For more depth into each step open the Jupyter file titled MarchMadnessScript.ipynb)

Language: Python (Jupyter)
<br>
IDE: VS Code
<br>
Libraries: Pandas, NumPy, Scikit-Learn
<br>
Machine Learning Algorithm(s): Fixed ensemble of Extra Trees and Random Forest

**Project Overview**
<br>
The March Machine Learning Mania 2025 competition tasked participants with forecasting the winners of NCAA tournament matchups for the 2025 season. Leveraging historical data provided by Kaggle—including regular season and tournament results, team seeds, and a sample submission format—I built predictive models evaluated using log loss. This project resulted in Stage 2 submissions.
<br><br>

**Methodology**
<br>
Data Preparation
I began by loading and processing the competition datasets using pandas, sourced from D:\march-machine-learning-mania-2025\. Key files included:

- WRegularSeasonDetailedResults.csv and MRegularSeasonDetailedResults.csv for regular season stats.
- WNCAATourneyDetailedResults.csv and MNCAATourneyDetailedResults.csv for tournament history.
- WNCAATourneySeeds.csv and MNCAATourneySeeds.csv for seeding data.
- SampleSubmissionStage2.csv for the prediction format.
- Matchups were segmented into men’s (Team IDs 1101-1484) and women’s (Team IDs 3101-3613) categories to account for differing team dynamics.

**Feature Engineering**
<br>
I developed a range of features to enhance model performance, including:

- Win Percentage: Calculated from regular season wins and losses.
- Margin of Victory (MOV): Average point differential per game.
- Seed Number: Extracted numerically from seed data (e.g., “W01” becomes 1), with missing seeds defaulting to 16.
- Offense and Defense Strength: Points scored and allowed per game.
- Last Five Win Rate: Success rate in the final five regular season games.
- Turnover Ratio: Average turnovers per game.
- Rebound Margin: Difference between team and opponent rebounds.

**Modeling Approach**
<br>
I employed scikit-learn’s ExtraTreesClassifier and RandomForestClassifier, combining their predictions into an ensemble. Key details:

- Utilized a fixed ensemble (60% ExtraTrees, 40% RandomForest) with initial features (e.g., win percentage, MOV, rebound margin). After much trial and error I landed on the most optimal hyper parameter tuning.

**Key Learnings**
<br>
- Feature Engineering Impact: Interactive features such as rebound margin improved log loss, underscoring the value of domain-specific features.
- Ensemble Effectiveness: Dynamic weighting based on log loss enhanced prediction accuracy compared to fixed weights.
- Data Preprocessing: Extensive merging and handling of missing data (e.g., seed defaults) were critical to model success.
- Log Loss Sensitivity: Balancing confidence in predictions was essential to avoid high penalties from incorrect strong predictions.

**Conclusion**
<br>
This project was a rewarding challenge that deepened my expertise in machine learning, feature engineering, and data analysis. The experience was invaluable, and I’m eager to apply these skills to future endeavors. For questions, feedback, or collaboration, please connect with me on LinkedIn: www.linkedin.com/in/gerry-jones-jr-72b448340.

Thank you for reviewing my work!
