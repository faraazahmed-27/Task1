# Task1: Data Cleaning & Preprocessing


Importing all the necessary Libraries

Missing-value imputation
Age → median (robust to skew)
Embarked → mode (most frequent port)
Fare → median (in case of test nulls)
Cabin → dropped ( > 70% missing)


Feature Engineering

Title: extracted from Name (e.g. “Mr.”, “Mrs.”) → groups rare ones into “Other”

FamilySize -> combines SibSp + Parch + 1


Encoding

One-hot encode Sex, Embarked, Title (drop first to avoid multicollinearity)
using pd.get_dummy() function


Scaling

Standardize Age, Fare, FamilySize to mean = 0, σ = 1 for algorithms sensitive to scale
this centers each feature at mean = 0 and rescales to unit variance:


Outliers

Visualized with boxplots
Removed rows where any standardized feature lies beyond ±3 σ


Correlation Check

Helps spot highly correlated features for further feature selection
