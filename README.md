

This project analyzes a student’s quiz performance data and provides personalized recommendations for improvement. Two datasets are used:
1. Current Quiz Data – Details of the most recent quiz submission.
2. Historical Quiz Data – The performance data from the last 5 quizzes including scores, accuracy, and response maps.

# Features

- Data Loading & Preprocessing: Reads JSON files and converts them into pandas DataFrames.
- Performance Analysis: Aggregates data by topics, computes average score, accuracy, and speed.
- Insight Generation: Highlights weak areas (topics with lower accuracy or scores), trends over time, and performance gaps.
- Personalized Recommendations: Provides actionable steps (e.g. focus on certain topics or practice specific question types) and a simple “student persona” label based on performance.
- NEET Rank Prediction (Bonus): A placeholder regression model predicts the student’s NEET rank based on performance metrics.
  
# Setup Instructions

1. Prerequisites:  
   - Python 3.8+ 
   - Install required packages using pip:
     ```bash
     pip install pandas numpy scikit-learn matplotlib
     ```
2. Files:  
   - `student_recommendations.py` – Main script.
   - `current_quiz_data.json` – JSON file containing the current quiz submission.
   - `historical_quiz_data.json` – JSON file containing historical quiz data.


4. Output:  
   - The script prints out insights, recommendations, and a student persona summary.
   - It also creates a simple matplotlib plot to show performance trends.

# Approach Overview

- Data Loading:  
  The script loads the JSON data using Python’s built-in `json` module and converts it into pandas DataFrames.
  
- Analysis:  
  Using pandas, it aggregates the historical quiz performance by topic and computes mean scores, accuracy, speed, etc. The script then identifies topics where the performance is below a set threshold.

- Recommendations:  
  Based on the computed metrics, the script recommends that the student review topics with lower average accuracy and suggests practice on question types (if available) or adjustment in time management.

- Student Persona:  
  A simple analysis assigns a persona label such as “Consistent Performer” or “Rapid but Inaccurate” based on the average accuracy and speed.

- NEET Rank Prediction:  
  Using scikit-learn’s LinearRegression, a very basic model is trained on historical performance (using features such as final_score, accuracy, speed, etc.) to predict the rank. (In practice, more training data and feature engineering would be required.)

.


