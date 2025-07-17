Iris Species Predictor API with FastAPI
=======================================

This project is a deployable machine learning API built using FastAPI. It predicts the species of Iris flowers (Setosa, Versicolor, or Virginica) based on their petal and sepal measurements.

--------------------------------------------------
🚀 Project Overview
--------------------------------------------------
- Model: Logistic Regression (Trained on Iris dataset)
- Framework: FastAPI (for REST API)
- Serving: Uvicorn (ASGI server)
- Libraries Used: scikit-learn, joblib, FastAPI, numpy

--------------------------------------------------
📁 Project Structure
--------------------------------------------------
iris_fastapi_project/
├── main.py              -> FastAPI app with prediction logic
├── schema.py            -> Pydantic schema for request validation
├── iris_model.pkl       -> Pre-trained ML model
├── requirements.txt     -> Python dependencies
└── README.txt           -> Project documentation (this file)

--------------------------------------------------
🔍 Sample API Usage
--------------------------------------------------

POST /predict

Input JSON:
{
  "sepal_length": 6.1,
  "sepal_width": 2.9,
  "petal_length": 4.7,
  "petal_width": 1.4
}

Expected Output:
{
  "predicted_species": "versicolor"
}

--------------------------------------------------
🧪 Running Locally
--------------------------------------------------

1. Clone the repository and install dependencies:

   git clone https://github.com/YOUR_USERNAME/iris-fastapi-deploy.git
   cd iris-fastapi-deploy
   pip install -r requirements.txt

2. Start the FastAPI server:

   uvicorn main:app --reload

3. Open Swagger docs in your browser:

   http://127.0.0.1:8000/docs

--------------------------------------------------
☁️ Deploying on Render (Free Hosting)
--------------------------------------------------

1. Push the code to GitHub
2. Go to https://render.com
3. Create a new Web Service
4. Connect your repo and set these settings:
   - Build Command: pip install -r requirements.txt
   - Start Command: uvicorn main:app --host 0.0.0.0 --port 10000

--------------------------------------------------
🧠 Model Information
--------------------------------------------------
- Dataset: Iris Dataset from UCI ML Repository
- Features: sepal_length, sepal_width, petal_length, petal_width
- Target: setosa, versicolor, virginica
- Algorithm: Logistic Regression with max_iter=200

--------------------------------------------------
👨‍💻 Author
--------------------------------------------------
Vishwas R. Kashyap  
Email: slrcrp229@gmail.com  
LinkedIn: https://www.linkedin.com/in/vishwas-r-kashyap-3283a8229/  
GitHub: https://github.com/vrk2626

--------------------------------------------------
📜 License
--------------------------------------------------
MIT License. Free to use for learning, educational, and deployment purposes.
