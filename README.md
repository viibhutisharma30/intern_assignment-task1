# Personalized Mentor Recommendation System (CLAT)

This project is a content-based recommendation system that helps CLAT aspirants find the most suitable mentors (CLAT toppers) based on their profiles and preferences.

---

## Problem Statement

Design a simple AI/ML-based model to recommend mentors to CLAT aspirants using user profile information, such as:

- Preferred legal subjects
- Target law colleges
- Preparation level
- Learning style

---

## Summary of the Approach

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

## Setup Instructions

### Clone the Repository or Download the Notebook

```bash
git clone https://github.com/yourusername/mentor-recommender-clat.git
cd mentor-recommender-clat
```
## How to Run
Run the notebook/script:

```
python mentor_recommender.py
```
Or open the .ipynb file in Jupyter and run all cells.

It will:

1. Generate mock aspirant and mentor profiles
2. Encode the features
3. Compute cosine similarity
4. Output the top 3 mentor recommendations for each aspirant

---

## Feedback Loop (Bonus)
A simulated feedback structure is included:
```
feedback = {
    1: {101: 5, 102: 4},  # Aspirant 1 gave ratings
    2: {104: 2, 106: 5}
}
```
This can be used later to:

1. Incorporate collaborative filtering
2. Refine mentor ranking
3.Collect mentor performance statistics

---

## Future Improvements
1. Add feature weighting (e.g., prioritize subject over style).
2. Incorporate NLP-based matching for open-text inputs.
3. Build a hybrid recommendation system using feedback and content.
4. Deploy with Streamlit or Flask for user interface.

---

## Sample Output
```
Aspirant 1 matches best with:
 - Mentor 102 (Similarity: 0.98)
 - Mentor 101 (Similarity: 0.96)
 - Mentor 106 (Similarity: 0.89)
```
