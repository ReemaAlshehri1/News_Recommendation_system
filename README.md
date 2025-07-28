# News_Recommendation_system

This AI-powered system recommends personalized news articles to users based on their interests and behavior. It leverages the [MIND dataset](https://msnews.github.io/) and provides recommendations using **content-based filtering** and **keyword-based extraction** models. It also includes a user-friendly interface built with Flask and ngrok

## Features
1. **Dual Recommendation Models**:  
   - Content-Based Filtering* using Sentence Transformers  
   - Keyword-Based Matching using KeyBERT  
2. **Real-Time Personalized Recommendations**:
   - Recommends top 5 relevant news articles based on user input and preferences
3. **Interactive Web Interface**:  
   - Built with Flask and styled with TailwindCSS  
   - Hosted via ngrok for public access in Colab or local environments  
4. **User Behavior Tracking**:  
   - Users can **like**, **dislike**, or **bookmark** news articles  
   - Feedback is saved in user_data.json and used to improve future recommendations  
5. **System Performance Dashboard**:  
   - Admin can monitor satisfaction rate based on user feedback  

## How to run
1. Clone the repository:
   git clone https://github.com/ReemaAlshehri/News_Recommendation_system
.git
   cd news-recommender
2. Install dependencies:
   pip install -r requirements.txt
4. download the dataset :
   - Download MINDsmall_train from here https://msnews.github.io/
   - Extract it inside the data/ folder
5. Preprocess the dataset:
   - Open and edit preprocess.py to set the correct dataset path
   - Then run it to generate the requierd data
6. Run the recommender pipeline :
   python recommender.py
7. Launch the app:
   python app.py

Note:
You can run this project in Google Colab or your local machine.
If running in Colab, use flask-ngrok to tunnel the app.

## GitHub structure
``` News_Recommendation_system/ ├── app.py # Flask app with routes and UI ├── recommender.py # Model loading and recommendation logic ├── preprocess.py # Dataset extraction and preprocessing ├── requirements.txt # List of dependencies ├── README.md # Project documentation ├── user_data.json # Stores user likes, dislikes, bookmarks ├── data/ # Folder for preprocessed data │ ├── news_preprocessed.csv # Cleaned and tokenized articles │ ├── news_embeddings.pkl # Embeddings for content-based filtering │ └── news_keywords.pkl # Extracted keywords for keyword-based matching ``` 
