# 🛡️ Phishing Website Detection  
This project uses supervised machine learning to **detect phishing websites** from a URL. The dataset consists of labeled URLs (phishing = `'bad'`, legitimate = `'good'`) and the URL.  

---

### 📌 Project Goal  
The goal is to train a **binary classification model** that predicts whether a website is **Phishing (0)** or **Legitimate (1)** while demonstrating end-to-end ML practices:  

- Data cleaning and preprocessing  
- Feature engineering from URLs  
- Handling class imbalance (SMOTE & class weighting)  
- Model training and optimization (Logistic Regression, Random Forest, XGBoost)  
- Evaluation using advanced metrics  

---

### ⚙️ Key Steps  
- **Feature Engineering**: Designed meaningful predictors from raw URLs.  
- **Train-Test Split**: Stratified 80/20 split to maintain class balance.  
- **Class Balancing**: Applied SMOTE oversampling on phishing sites.  
- **Scaling**: Standardized numerical features before training.  
- **Modeling**:  
  - Logistic Regression → baseline  
  - Random Forest → tuned with RandomizedSearchCV and probability thresholding 
  - XGBoost → tuned with RandomizedSearchCV and probability thresholding  

---
### 🛠️ Features Engineered:
- digit_count
- url_word_count
- url_entropy
- path_length
- special_char_count
- vowel_ratio
- char_diversity
- longest_word_length
- consecutive_digits
- consecutive_consonants
- alnum_ratio
- digit_to_char_ratio
- num_dots
- num_hyphens
- uppercase_ratio
- hostname_length
- query_length
- param_count
- has_at
- has_https
- has_ip_address
- num_slashes
- repeated_char_count
- subdomain_count
- suspicious_word_count

**Features Used in Final Model:**
- digit_count
- url_word_count
- url_entropy
- path_length
- special_char_count
- vowel_ratio
- char_diversity
- longest_word_length
- consecutive_digits
- consecutive_consonants
- alnum_ratio
- digit_to_char_ratio
- num_dots
- num_hyphens
- uppercase_ratio

---

### 📊 Evaluation Metrics  
Models were assessed on the following:

- **Accuracy**  
- **Precision / Recall / F1-score**  
- **ROC AUC (discrimination ability)**
- 
---

### 🤖 Best Performing Model  
✅ **Random Forest Classifier** (tuned):  

- Accuracy: **0.92**  
- Precision (Phishing): **0.87**  
- Recall (Phishing): **0.84**  
- F1 Score (Phishing): **0.85**  
- ROC AUC: **0.97**  

XGBoost also performed strongly but required more tuning to balance recall and precision.  

---

### 📁 Files Included  
- `Phishing_Website_Detection.ipynb`: Full code notebook with preprocessing, modeling, and evaluation  
- `phishing.csv`: Dataset (processed version)  
- `README.md`: Project overview and documentation  

---

###🏷️ Tags  
#MachineLearning #Classification #Cybersecurity #PhishingDetection #RandomForest #XGBoost #DataScience #Sklearn  

---

Project by Andres Figueroa  
