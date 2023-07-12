# Phising Website Detection

This repository contains the following files:

1. `phishing.ipynb`: This Jupyter Notebook file contains code for a machine learning model to predict phishing websites. It includes data preprocessing, feature extraction, model training, and evaluation. The notebook also includes visualizations of the data and the trained model's performance.

2. `phishing.pkl`: This file is a serialized version of the trained machine learning model. It can be loaded and used for predictions without retraining the model.

3. `app.py`: This Python file implements a FastAPI application that uses the trained model to make predictions on incoming requests. It provides an API endpoint `/predict/{feature}` where you can pass a website URL as the `feature` parameter, and it will return a prediction whether the website is a phishing site or not.

## Installation

To run the code and use the trained model, follow these steps:

1. Clone the repository:

   ```
   git clone https://github.com/Phishing-Website-Detection.git
   ```

2. Install the required Python libraries:

   ```
   pip install pandas numpy seaborn matplotlib scikit-learn nltk wordcloud bs4 selenium networkx uvicorn fastapi joblib
   ```

3. Download the dataset file (`phishing_site_urls.csv`) and place it in the same directory as the Jupyter Notebook (`phishing.ipynb`).

4. Run the Jupyter Notebook (`phishing.ipynb`) to train the model, perform data analysis, and generate the serialized model file (`phishing.pkl`).

5. To run the FastAPI application, execute the following command in your terminal:

   ```
   uvicorn app:app --reload
   ```

   The API server will start running locally at `http://localhost:8000`.

## Usage

### Jupyter Notebook

Open the `phishing.ipynb` file in Jupyter Notebook or Jupyter Lab. Run the notebook cells to execute the code step by step. This will train the model, visualize the data, and evaluate the model's performance. You can modify the code or experiment with different techniques as needed.

### FastAPI Application

1. Ensure that the FastAPI application is running by executing the command:

   ```
   uvicorn app:app --reload
   ```

2. Open a web browser or use an API testing tool (e.g., Postman) and make a GET request to the following endpoint:

   ```
   http://localhost:8000/predict/{feature}
   ```

   Replace `{feature}` with the URL of the website you want to predict. The application will return a JSON response with the website URL and the prediction result (phishing or not phishing).

## Contributing

Contributions are welcome! If you find any issues or want to enhance this project, feel free to open a pull request.
