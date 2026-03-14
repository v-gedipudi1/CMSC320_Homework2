import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
from scipy.stats import ttest_ind
import os

# Making sure these match the files in my folder exactly!
files = [
    "Dataset Generation (2024) (Responses) - Form Responses 1.csv",
    "Dataset Generation (Fardina) (Responses) - Form Responses 1.csv",
    "Dataset Generation (Max) (Responses) - Form Responses 1.csv",
    "Dataset Generation (Spring 2025) (Responses) - Form Responses 1.csv",
    "Dataset Generation Responses (Spring 2026).csv",
    "Spring 2026 Response Data - Sheet1.csv"
]

all_data = []

# Cleaning the loop
for f in files:
    try:
        data = pd.read_csv(f)
        
        # Finding the doctor column by searching for the word "doctor"
        target_col = [c for c in data.columns if 'doctor' in c.lower()][0]
        
        # Checks the actual text to see if it's "boyfriend" or "girlfriend"
        sample_text = target_col.lower()
        if 'boyfriend' in sample_text or 'son' in sample_text or 'husband' in sample_text:
            gender_label = 'Male'
        else:
            gender_label = 'Female'
            
        # Creates a small dataframe with just what I need
        subset = data[[target_col]].copy()
        subset.columns = ['rating']
        subset['story_gender'] = gender_label
        all_data.append(subset)
    except Exception as e:
        print(f"Skipping file {f} due to error: {e}")

# Merges all the years together
final_df = pd.concat(all_data).dropna()

# Turns text into numbers for the T-Test
mapping = {"Not a jerk": 0, "Mildly a jerk": 1, "Strongly a jerk": 2}
final_df['score'] = final_df['rating'].map(mapping)

# Hypothesis test
male_grp = final_df[final_df['story_gender'] == 'Male']['score']
female_grp = final_df[final_df['story_gender'] == 'Female']['score']
t_stat, p_val = ttest_ind(male_grp, female_grp)

print("\n--- STATS RESULTS ---")
print(f"T-Statistic: {t_stat}")
print(f"P-Value: {p_val}")
print("----------------------\n")

# For the theme
sns.set_theme(style="white") 
plt.figure(figsize=(8, 5))

# Plotting the data
sns.barplot(
    data=final_df, 
    x='story_gender', 
    y='score', 
    hue='story_gender',
    palette='magma', 
    capsize=.1,
    legend=False
)

# Professional labels
plt.title("Student Moral Judgments by Character Gender", fontsize=14)
plt.xlabel("Gender of the Character in the Story", fontsize=12)
plt.ylabel("Avg Jerk Score (0-2)", fontsize=12)
plt.ylim(0, 2) 
sns.despine() 

save_path = os.path.join(os.getcwd(), "final_analysis_plot.png")
plt.tight_layout()
plt.savefig(save_path, dpi=300)

print(f"SUCCESS: The plot has been saved to your folder as: final_analysis_plot.png")
print("Look at the sidebar on the left of VS Code and click the file to see it!")

plt.show() 
