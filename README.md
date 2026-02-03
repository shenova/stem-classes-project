# Are STEM Classes Substantively Different from Non-STEM Classes?

This project explores whether STEM and non-STEM university courses differ meaningfully in terms of student experience. Using UC San Diego course evaluation data, we apply machine learning techniques to test whether courses can be accurately classified as STEM or non-STEM based on student-reported outcomes.

**Authors:** Evelyn Kimbirk, Cameron Faulkner, Shenova Davis  
**Course:** COGS 118B  
**Institution:** UC San Diego

---

## Motivation

As STEM degrees have become increasingly popular, there is a common perception that STEM courses are more difficult, time-consuming, and less enjoyable than non-STEM courses. Rather than relying on anecdotal claims or grades alone, this project investigates whether measurable differences in student experience exist between STEM and non-STEM classes.

Our core research question is:

> **Are STEM classes substantively different from non-STEM classes?**

---

## Data

We use student evaluation data from UC San Diego’s Course and Professor Evaluations (CAPEs), collected by the SeasCAPE project.

- **Time span:** Fall 2017 – Summer 2020  
- **Total observations:** 9,981 course instances  
- **Source:** SeasCAPE (UCSD)

### Key Features Used
- Percentage of students who recommend the class  
- Percentage of students who recommend the instructor  
- Average hours spent per week  
- Average GPA for the course  

Courses were labeled as **STEM or non-STEM** based on department codes.

---

## Methodology

To test whether student experience differs between STEM and non-STEM classes, we trained a **Support Vector Machine (SVM)** classifier.

### Why SVM?
- Effective for binary classification
- Performs well with small feature sets
- Suitable for identifying subtle patterns in high-dimensional data

### Model Setup
- **Target variable:** STEM vs. non-STEM (binary)
- **Features:** Recommendation rates, time spent, GPA
- **Train/Test Split:** 80% / 20%
- **Evaluation Metrics:** Accuracy, precision, recall, F1-score, confusion matrices

---

## Results

### Test Set Performance
- **Overall accuracy:** ~76%
- **STEM recall:** ~78%
- **Non-STEM recall:** ~74%

While the model performs better than random guessing (50%), it does not achieve strong separation between the two groups.

### Interpretation
- The classifier identifies a **weak but consistent signal**
- Similar training and test accuracy suggests minimal overfitting
- Results imply **only modest differences** in student experience between STEM and non-STEM courses

---

## Key Takeaways

- STEM and non-STEM classes are **not drastically different** when measured by student evaluations
- Differences exist, but they are **subtle rather than substantial**
- Student experience is influenced by more than just course type

---

## Limitations & Future Work

- Data is limited to **one institution (UCSD)**, which is STEM-focused
- STEM classification was done at the **department level**, not course content level
- Future work could:
  - Include multiple universities
  - Refine STEM labeling at the course level
  - Explore additional student experience metrics

---

## References

- SeasCAPE Project: https://github.com/dcao/seascape  
- Tomkin & West (2022), *STEM Courses Are Harder*  
- Winters-Hilt & Merat (2007), *SVM Clustering*

---

## Technologies Used

- Python  
- pandas, NumPy  
- scikit-learn  
- matplotlib  

---

## Full Paper

The full report and analysis are available in the accompanying PDF:

📄 **Report and Code.pdf** :contentReference[oaicite:0]{index=0}
