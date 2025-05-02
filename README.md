# 📰 Personalized News Recommendation System

This project is a hybrid recommendation system that suggests relevant news articles to users based on **Collaborative Filtering** and **Content-Based Filtering**.

It simulates real-world systems used by platforms like Google News or Netflix to personalize content for individual users.

---

## 📽️ Project Demo

▶️ **Watch the Presentation Video**:  
[![Watch on Loom] (https://www.loom.com/share/407b829a626c4d71b3516f421b83f946)]

---

## 📌 Features

- Simulated user-article interaction matrix
- Collaborative filtering using cosine similarity
- Content-based filtering using TF-IDF on news titles
- Combined recommendation output for each user
- Clean and readable output tables

---

## 📁 Dataset

The dataset is a line-delimited JSON file, where each line represents a news article:

```json
{"category": "PARENTING", "headline": "Jimmy Kimmel Challenge: Parents 'Silverstone' Their Kids' Food", ...}
```

Each record includes:
- `category`
- `headline`
- `short_description`
- `link`
- `authors`
- `date`

---

## 🧠 How It Works

### ✅ Step 1: Data Preparation
- Load the JSON data into a Pandas DataFrame
- Extract useful fields such as `title`, `category`, `short_description`

### ✅ Step 2: Simulate User Interaction
- Created a user-article interaction matrix with mock data
- This mimics user behavior like article clicks or reads

### ✅ Step 3: Collaborative Filtering
- Compute cosine similarity between user vectors
- Recommend articles that similar users found interesting

### ✅ Step 4: Content-Based Filtering
- Use TF-IDF on article titles to represent content
- Compute similarity of articles based on textual content
- Recommend similar articles to those the user already liked

### ✅ Step 5: Combine Recommendations
- Merge top collaborative and content-based recommendations
- Present unified recommendations with category mapping

---

## 🧪 Example Output

**Recommendations for `user_1`:**

| Title                                                  | Category        |
|--------------------------------------------------------|-----------------|
| American Airlines Flyer Charged...                     | U.S. NEWS       |
| Mark Meadows Complies With Justice Dept. Subpoena...   | POLITICS        |
| Puerto Ricans Desperate For Water...                   | WORLD NEWS      |
| Meet Alex Aster, The TikToker...                       | CULTURE & ARTS  |
| Possible Nationwide Rail Strike...                     | U.S. NEWS       |

---

## 🚀 Technologies Used

- Python
- Pandas
- Numpy
- Scikit-learn
- TF-IDF (Natural Language Processing)
- Cosine Similarity

---

## 📌 Future Improvements

- Integrate real user interaction logs (views, clicks)
- Use full article text (not just title) for content filtering
- Deploy the system using Streamlit or Flask
- Enable real-time recommendations via REST API

---
