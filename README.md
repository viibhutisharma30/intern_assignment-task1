# 🧑‍🏫 Personalized Mentor Recommendation System (CLAT)

This project is a content-based recommendation system that helps CLAT aspirants find the most suitable mentors (CLAT toppers) based on their profiles and preferences.

---

## 📌 Problem Statement

Design a simple AI/ML-based model to recommend mentors to CLAT aspirants using user profile information, such as:

- Preferred legal subjects
- Target law colleges
- Preparation level
- Learning style

---

## 🧠 Summary of the Approach

We implemented a **content-based filtering recommendation system** using **cosine similarity**:

1. **Mock data** of 50 aspirants and 10 mentors was generated with features:
   - Subject preference / expertise
   - Target college / alumni college
   - Learning / mentoring style
2. **Label Encoding** was used to convert categorical features into numerical vectors.
3. **Cosine similarity** was computed between aspirant and mentor feature vectors.
4. For each aspirant, the top 3 mentors with the highest similarity scores were recommended.
5. Optionally, a feedback structure was added to allow user rating collection for future model improvement.

---

## ⚙️ Setup Instructions

### 1. Clone the Repository or Download the Notebook

```bash
git clone https://github.com/yourusername/mentor-recommender-clat.git
cd mentor-recommender-clat
