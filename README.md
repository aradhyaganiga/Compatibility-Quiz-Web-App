# 💍 Divorce Prediction & Compatibility Web App

A smart, ML-powered web application that predicts **divorce risk** for married couples and **compatibility score** for unmarried couples using structured questionnaires and partner-based analysis.

This project combines **Flask**, **Machine Learning**, and **Relational Databases** to deliver meaningful relationship insights in a simple and interactive way.

---

## ✨ Features

- 🔘 Choose **Married / Unmarried**
- 👤 Gender-based questionnaire (Male / Female)
- 📝 Psychology-inspired questions with weighted options
- 🔗 Unique shareable link for partner
- 🤝 Dual-user response aggregation
- 🧠 Machine Learning prediction
  - Married → Divorce Risk %
  - Unmarried → Compatibility %
- 📊 Clear result interpretation with advice
- 🔐 Privacy-first design (no unnecessary personal data)

---

## 🧭 Application Flow

1. User opens the website
2. Selects **Married** or **Unmarried**
3. Selects **Gender**
4. Answers questionnaire
5. App generates a **unique link**
6. Partner opens the link and answers
7. Domain-wise score seggregation processes both responses
8. Result is displayed

---

## 🛠️ Tech Stack

### Frontend
- HTML5
- CSS3
- JavaScript

### Backend
- Python
- Flask

### Database
- SQLite (can be upgraded to MySQL / PostgreSQL)

### Machine Learning
- scikit-learn
- Feature Engineering + Threshold Logic

---

## 🗃️ Database Design (Overview)

### Tables
- `questions` – stores questionnaire text
- `options` – answer options with weights
- `pair_links` – unique couple links
- `responses` – individual answers
- `results` – ML prediction output

---

## 🧠 Machine Learning Logic

### Feature Engineering
- Domain-wise score aggregation
- Partner score differences
- Overall compatibility metrics

### Prediction Logic
- Married → Divorce Risk Probability
- Unmarried → Compatibility Score

```python
if probability > threshold:
    label = "High Risk"
else:
    label = "Low Risk"

