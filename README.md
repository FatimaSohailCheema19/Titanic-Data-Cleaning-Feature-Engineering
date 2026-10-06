# 🚢 Titanic Data Cleaning & Feature Engineering

A data mining project focused on **cleaning, preprocessing, and feature engineering** using the Titanic Survival Dataset.

The objective of this project was to transform the raw Titanic dataset into a clean and structured dataset that can be used for further analysis or machine learning tasks.

---

## 📌 Project Overview

The Titanic dataset contains passenger information such as:

- Passenger class
- Age
- Sex
- Family relationships
- Ticket information
- Fare
- Cabin
- Port of embarkation
- Survival status

The raw dataset contains missing values and categorical information that require preprocessing before predictive modeling can be performed.

This project focuses on:

- Handling missing values
- Creating useful new features
- Encoding categorical variables
- Removing unnecessary columns
- Preparing the final dataset for analysis and machine learning

---

## 🎯 Objective

The main objective was to clean and prepare the Titanic Survival Dataset so that it could be used effectively for future modeling.

The preprocessing pipeline aimed to:

- Remove or handle missing data
- Improve the quality of available features
- Create meaningful derived variables
- Convert categorical variables into numerical form
- Produce a final dataset without missing values

---

## 📊 Dataset Overview

The Titanic dataset contains **891 passenger records**.

Important columns include:

- PassengerId
- Survived
- Pclass
- Name
- Sex
- Age
- SibSp
- Parch
- Ticket
- Fare
- Cabin
- Embarked

The target variable is:

**Survived**

where:

- `0` = Passenger did not survive
- `1` = Passenger survived

---

## 🧹 Handling Missing Values

Several columns contained missing values in the original dataset.

The following strategies were used:

### Age

Missing values in the **Age** column were filled using the median age.

The median was selected because age values can contain outliers, and the median is less sensitive to extreme values.

---

### Embarked

Missing values in the **Embarked** column were filled using the mode.

The mode represents the most frequently occurring embarkation port.

---

### Fare

Missing Fare values were filled using the median fare.

---

### Cabin

The Cabin column contained a large number of missing values.

Instead of directly filling the missing Cabin values, a new feature called:

**CabinKnown**

was created.

The feature represents whether cabin information was available:

- `1` = Cabin information is available
- `0` = Cabin information is missing

The original Cabin column was then removed.

---

## 🧩 Feature Engineering

Several new features were created to improve the dataset.

### 🎭 Title Extraction

Passenger titles were extracted from the **Name** column.

Examples include:

- Mr
- Mrs
- Miss

Less common titles were grouped into a single category:

**Rare**

This allows information from passenger names to be retained in a structured form.

---

### 👨‍👩‍👧 Family Size

A new feature called **FamilySize** was created.

It represents the total number of family members traveling with each passenger.

The feature was calculated using:

**FamilySize = SibSp + Parch + 1**

where:

- SibSp = Number of siblings/spouses aboard
- Parch = Number of parents/children aboard
- `+1` represents the passenger themselves

---

### 🧍 Alone Indicator

A new feature called **Alone** was created.

It identifies whether a passenger was traveling alone.

- `1` = Passenger was alone
- `0` = Passenger was traveling with family

---

### 🎟️ Ticket Group Size

A new feature called **TicketGroup** was created.

This feature represents the number of passengers sharing the same ticket.

It can provide useful information about passengers traveling together.

---

## 🔢 Encoding Categorical Variables

Categorical variables were converted into numerical indicator variables using dummy encoding.

The following features were encoded:

- Sex
- Embarked
- Title

The resulting encoded columns include:

- Sex_male
- Embarked_Q
- Embarked_S
- Title_Miss
- Title_Mr
- Title_Mrs
- Title_Rare

The first category was dropped during encoding to reduce unnecessary redundancy.

---

## 🗑️ Dropping Unnecessary Columns

After feature engineering, the following original columns were removed:

- Name
- Ticket
- Cabin

These columns were no longer required because their useful information had already been extracted into new features.

---

## ✅ Final Cleaned Dataset

After preprocessing, the final dataset contains **20 columns**.

The final dataset includes:

- PassengerId
- Survived
- Pclass
- Age
- SibSp
- Parch
- Fare
- CabinKnown
- FamilySize
- Alone
- TicketGroup
- Sex_male
- Embarked_Q
- Embarked_S
- Title_Miss
- Title_Mr
- Title_Mrs
- Title_Rare

All missing values were successfully handled.

The dataset is now ready for:

- Exploratory Data Analysis
- Survival prediction
- Classification models
- Feature importance analysis
- Further machine learning experiments

---

## 📁 Repository Structure

Titanic-Data-Cleaning-Feature-Engineering/

├── report/

│   └── Titanic_Data_Cleaning_Report.pdf

│

├── screenshots/

│   ├── original_dataset_info.png

│   ├── cleaned_dataset_preview.png

│   └── missing_values_after_cleaning.png

│

└── README.md

---

## 📸 Screenshots

The **screenshots/** folder contains visual evidence of the preprocessing process.

### Original Dataset Information

Shows the original Titanic dataset structure and missing values before preprocessing.

Important missing values included:

- Age
- Cabin
- Embarked

---

### Cleaned Dataset Preview

Shows the transformed dataset after:

- Missing value handling
- Feature engineering
- Categorical encoding

The preview includes engineered features such as:

- CabinKnown
- FamilySize
- Alone
- TicketGroup
- Encoded Sex
- Encoded Embarked
- Encoded Title variables

---

### Missing Values After Cleaning

The final verification confirms that all columns contain:

**0 missing values**

This indicates that the preprocessing process successfully prepared the dataset for further analysis.

---

## 📄 Project Report

The complete assignment report is available in:

**report/Titanic_Data_Cleaning_Report.pdf**

The report contains:

- Introduction
- Dataset overview
- Missing value handling
- Feature engineering
- Categorical encoding
- Column removal
- Final cleaned dataset
- Sample output
- Summary of preprocessing steps

---

## 🧠 Key Learning Outcomes

Through this project, I practiced:

- Data inspection
- Missing value analysis
- Median imputation
- Mode imputation
- Feature engineering
- String-based feature extraction
- Categorical encoding
- Dummy variables
- Dataset restructuring
- Data preparation for machine learning

---

## 🔍 Key Features Created

The main engineered features were:

**CabinKnown**  
Indicates whether cabin information was available.

**FamilySize**  
Represents the total size of the passenger's family aboard the ship.

**Alone**  
Indicates whether the passenger was traveling alone.

**TicketGroup**  
Represents the number of passengers sharing the same ticket.

**Title**  
Extracts useful social information from passenger names and groups uncommon titles into a Rare category.

---

## 🚀 Possible Future Work

The cleaned dataset can be extended into a complete Titanic survival prediction project.

Possible future improvements include:

- Exploratory Data Analysis
- Survival visualization
- Logistic Regression
- Decision Trees
- Random Forest
- K-Nearest Neighbors
- Support Vector Machines
- Model comparison
- Hyperparameter tuning
- Feature importance analysis
- Cross-validation

---

## 🎓 Academic Context

This project was completed as part of a **Data Mining Lab assignment**.

The objective was to gain practical experience in data cleaning, preprocessing, feature engineering, and preparing raw data for machine learning.

---

## 👩‍💻 Authors

**Fatima Sohail**  
**Namra Noor**

BS Data Science  
GIFT University

---

## ⭐ Support

If you find this data cleaning project useful for learning preprocessing or feature engineering, consider giving the repository a ⭐.
