# 🎬 End-to-End Movie Recommendation System

![Hero Image](assets/hero.png)

## 🌟 Overview
A state-of-the-art movie recommendation engine that combines **TF-IDF Content-Based Filtering** with real-time data from the **TMDB API**. This project offers a seamless experience from data exploration to a fully interactive web application.

Developed by **[manasscodes](https://github.com/manasscodes)**.

---

## 🚀 Features
- **🔍 Intelligent Search**: Find movies with real-time suggestions and keyword matching.
- **🎯 Personalized Recommendations**: Get suggestions based on plot similarity (TF-IDF) and genre metadata.
- **📱 Responsive UI**: A modern, sleek interface built with Streamlit and custom CSS.
- **⚡ Fast Backend**: Powered by FastAPI for high-performance recommendation serving.
- **📊 Data-Driven**: Utilizes a cleaned dataset of thousands of movies with pre-computed TF-IDF matrices.

---

## 🛠️ Tech Stack
- **Frontend**: [Streamlit](https://streamlit.io/)
- **Backend**: [FastAPI](https://fastapi.tiangolo.com/)
- **Data Science**: Pandas, NumPy, Scikit-learn (TF-IDF, Cosine Similarity)
- **API**: [The Movie Database (TMDB)](https://www.themoviedb.org/documentation/api)
- **Deployment Ready**: Modular structure optimized for modern cloud platforms.

---

## 📂 Project Structure
```text
.
├── app/
│   ├── frontend.py        # Streamlit Web Application
│   └── backend.py         # FastAPI Recommendation Engine
├── data/
│   ├── raw/               # Original datasets (CSV)
│   └── processed/         # Serialized models and processed data (Pickles)
├── notebooks/
│   └── movie_exploration.ipynb  # Data analysis and model training logic
├── assets/                # UI assets and documentation images
├── .env.example           # Template for environment variables
├── requirements.txt       # Python dependencies
└── README.md              # Project documentation
```

---

## ⚙️ Setup & Installation

### 1. Clone the Repository
```bash
git clone https://github.com/manasscodes/End-to-End_Movie-Recommendation-System.git
cd End-to-End_Movie-Recommendation-System
```

### 2. Configure Environment
Create a `.env` file in the root directory:
```bash
cp .env.example .env
```
Add your **TMDB API Key** to the `.env` file:
`TMDB_API_KEY=your_key_here`

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Run the Application
Start the backend server:
```bash
uvicorn app.backend:app --reload
```
In a new terminal, start the Streamlit frontend:
```bash
streamlit run app/frontend.py
```

---

## 🧪 How it Works
1. **Data Processing**: The `notebooks/movie_exploration.ipynb` processes movie metadata, generates tags, and builds a TF-IDF vectorizer.
2. **Similarity Scoring**: When a movie is selected, the backend calculates the cosine similarity between its vector and all other movies in the dataset.
3. **Hybrid Engine**: Results are enriched with real-time genre-based recommendations from TMDB to ensure fresh and relevant suggestions.

---

## 🤝 Contributing
Contributions are welcome! Feel free to open an issue or submit a pull request.

---

## 📜 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
