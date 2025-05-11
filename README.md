# 🎥 YouTube Kids Recommendation System

A smart, age-appropriate video recommendation system for kids, powered by the YouTube Data API. This tool dynamically fetches educational and entertaining videos based on a child’s age and subject preference.

---

## 📌 Features

- 🎯 Age-based query filtering using a custom CSV mapping
- 📚 Subject filtering (Science, Math, Geography, etc.)
- 🔍 Real-time video search from YouTube
- 📊 Fetch video metadata (views, likes, description, etc.)
- 💾 Save recommendations to CSV
- ☁️ Upload mapping and results to GitHub directly from Colab

---

## 🗂️ Project Structure

```
├── age_query_mapping.csv     # Mapping of age groups to queries and categories
├── youtube_kids_data.csv     # Output of recommended videos
├── RecommendationSystem.ipynb       # Google Colab notebook with full logic
├── EnhancedRecommendationSystem.ipynb       # Google Colab notebook with full logic
├── README.md                 # Project overview
```

---

## 🧠 How It Works

1. User enters the child's age and an optional subject.
2. Queries relevant to the age and subject are selected from `age_query_mapping.csv`.
3. YouTube Data API v3 is used to fetch live video metadata.
4. Top N videos are recommended, sorted by view count or relevance.

---

## 📁 Sample Mapping Format

| query                          | age_min | age_max | category     |
|-------------------------------|---------|---------|--------------|
| nursery rhymes for toddlers   | 3       | 5       | Music        |
| science for kids age 6 to 8   | 6       | 8       | Science      |
| solar system for kids         | 9       | 12      | Space        |

---

## 💡 Example Usage in Colab

```python
age = 8
subject = "Science"
recommendations = recommend_for_age_and_subject(age, subject)
recommendations.to_csv("youtube_kids_data.csv")
```

---

## ⚙️ Setup Instructions

1. Clone the repo or open the notebook in Google Colab.
2. Install required packages:
   ```bash
   pip install google-api-python-client pandas
   ```
3. Generate a YouTube API key from Google Developer Console.
4. Run the notebook to start generating age-based recommendations.

---

## 🔐 Security

- API Key and GitHub Token are securely entered via `getpass` in Colab.
- No sensitive data is hardcoded or exposed.

---

## 🙋‍♂️ Author

**Shilpa Thota**  
GitHub: [shilpathota](https://github.com/shilpathota)  
LinkedIn: https://www.linkedin.com/in/shilpa-thota/

---

## 📄 License

This project is open-source and intended for educational and personal use.  
Please respect YouTube’s API Terms of Service.
