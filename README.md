initialized fullstack
# Google Play Store Apps Prediction Website

## Overview
This project implements a website that features an API interacting with a Machine Learning model trained on a Google Play Store Apps dataset. The website is designed with an attractive and user-friendly UI/UX, containerized using Docker, and includes a CI/CD pipeline with GitHub Actions. The dataset has been pre-processed, and the model is versioned using MLFlow. The website is implemented using Streamlit and FastAPI.

## Dataset
We used the [Google Play Store Apps dataset](https://www.kaggle.com/datasets/lava18/google-play-store-apps) from Kaggle. The dataset has been analyzed, cleaned, transformed, and pre-processed before training the models. The dataset is divided into three phases to simulate the data drifting process. Each phase introduces new data, and we monitor the drift accordingly. The dataset is versioned and stored on Google Drive.

## Prediction
After thorough research and analysis of the dataset, we identified interesting features to predict, such as the app rating or category prediction based on other app features. The final model and predictions are based on these insights.

## Machine Learning Model
We trained several classification models, with a preference for Decision Trees, to make predictions based on the dataset. The models are versioned using MLFlow, allowing for easy tracking and updating of model versions. The latest model version is fetched by the API for prediction tasks.

## Website
The website is built using Streamlit for the frontend and FastAPI for the backend. It provides an intuitive interface for users to interact with the model. The website fetches the latest version of the trained model from MLFlow, ensuring that predictions are made using the most up-to-date model.


## GitHub Structure
This project utilizes Git submodules to organize the frontend and backend. To clone the repository with all submodules, use:
git clone https://github.com/hadi-karnib/hackathon-full.git.
If you've already cloned the repository, you can initialize and update the submodules using:
git submodule init
git submodule update
The project also includes a robust CI/CD pipeline, set up using GitHub Actions, which automates the testing, building, and deployment processes. Designated leaders from FSD and FSW teams (Json Greich and Hadi Karnib) are responsible for reviewing and approving pull requests to the main branch.

## Setup and Installation

### Prerequisites
- Python 3.x
- Docker
- Node.js

### Installation

1. *Clone the repository:*
   git clone https://github.com/hadi-karnib/hackathon-full.git
Navigate to the frontend directory and set up the virtual environment:
cd react-app
npm i
npm start
cd streamlit
pip install streamlit 
streamlit run python-streamlit


Navigate to the backend directory and set up the virtual environment:

/venv/Scripts/activate
pip install -r requirements.txt
cd Model
uvicorn predict:app --reload

