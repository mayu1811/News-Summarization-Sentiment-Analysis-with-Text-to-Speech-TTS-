# News Summarization & Sentiment Analysis with Text-to-Speech (TTS)

This project implements a news summarization and sentiment analysis tool that scrapes news articles, performs sentiment classification, compares sentiments across articles, and generates a Hindi audio summary of the results.

## 🚀 Features

- **News Scraping**: Fetches news articles related to a given company.
- **Sentiment Analysis**: Analyzes the sentiment of news articles (Positive, Negative, or Neutral).
- **Comparative Sentiment Analysis**: Provides a sentiment report comparing the articles.
- **Text-to-Speech**: Generates a Hindi audio summary of the sentiment report using `gTTS`.
- **Web Interface**: A user-friendly Streamlit app that displays the results.

## 🛠️ Project Setup

Follow the steps below to set up the project.

1️⃣ Clone the Repository

Clone the repository to your local machine:


2️⃣ Set Up Virtual Environment
Create a virtual environment and activate it:


python -m venv venv
source venv/bin/activate  # On Windows use venv\Scripts\activate


3️⃣ Install Dependencies
Install the required libraries listed in requirements.txt:


pip install -r requirements.txt
4️⃣ Run the Backend API
The backend API is built using FastAPI. Start the backend server using uvicorn:

uvicorn api:app --reload
The API will run on http://127.0.0.1:8000.

5️⃣ Run the Streamlit Frontend
Start the Streamlit app by running:

streamlit run app.py
This will launch the frontend on http://localhost:8501.

6️⃣ Deploy to Hugging Face Spaces
Go to Hugging Face Spaces.

Create a new space and select Streamlit.

Connect your GitHub repository to Hugging Face Spaces.

7️⃣ Access the Application
Once the Streamlit app is running, visit the URL provided by Streamlit or Hugging Face Spaces to use the application.

📚 Modules Breakdown

1️⃣ news_scraper.py
This module scrapes 10 news articles related to the input company using Google News.

2️⃣ sentiment_analysis.py
Uses NLTK VADER to analyze the sentiment of news article titles.

3️⃣ comparative_analysis.py
Compares the sentiment across all fetched news articles.

4️⃣ text_to_speech.py
Generates a Hindi audio summary of the sentiment analysis using gTTS.

5️⃣ api.py
Handles API requests using FastAPI. It integrates all modules and exposes a /analyze/{company} endpoint.

6️⃣ app.py
This is the frontend built using Streamlit. It allows users to input a company name, fetches data from the backend, and displays the results.

🧰 Requirements
The following libraries are required for this project:

streamlit: For the frontend interface.

beautifulsoup4: For scraping news articles.

requests: For making HTTP requests to fetch news.

nltk: For sentiment analysis.

transformers: For NLP tasks (optional for model-based tasks).

torch: For machine learning (if any models are used).

gtts: For text-to-speech conversion.

Flask, FastAPI, uvicorn: For creating the backend API.

To install these dependencies, run:

pip install -r requirements.txt

⚙️ How It Works
The Streamlit frontend takes a company name as input.

The frontend sends a request to the FastAPI backend, which scrapes news articles related to the company.

The backend performs sentiment analysis on the article titles using NLTK VADER.

A comparative sentiment analysis is performed, and a summary of the sentiments is generated.

A gTTS Hindi audio summary is generated and returned to the frontend.

The results are displayed in the Streamlit UI, along with the audio file.

📝 License
This project is open-source and available under the MIT License.

🗣️ Feedback & Contributions
Feel free to submit issues, pull requests, or suggestions. Contributions are welcome!

🚀 Next Steps
Enhance sentiment analysis by using more advanced models.

Add more language support for text-to-speech.

Implement better error handling and input validation.

[Hugging Face Link:](https://huggingface.co/spaces/mayur1811/NewsSummarizationSentimentAnalysiswithText-to-Speech)

[Demo Video Link:](https://go.screenpal.com/watch/cTe0Dmni3mc)
