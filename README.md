# 🚗 **Car Price Prediction App**

This project is a **machine learning-based web application** built with **Streamlit** to predict the price of used cars. Users can input key features of a car, such as mileage, engine capacity, age, and transmission type, and get an estimated price using a pre-trained **Random Forest Regressor** model.

## **📑 Table of Contents**

- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Model Training and Tuning](#model-training-and-tuning)
- [Contributing](#contributing)

## **📖 Overview**

The **Car Price Prediction App** allows users to predict the resale value of a car based on its features, using a machine learning model trained on historical car sales data. The app features an intuitive interface to make it easy for users to input car details and receive instant price predictions.

### **New in `app_final.py`:**
- Two separate sections for **Car Specifications** and **Other Details** to streamline the input process.
- Dynamic filtering of models, variants, and fuel types based on the selected manufacturer.
  
## **🔧 Features**

- **Input Fields for Car Features**:  
  - Manufacturer, Car Model, Variant, Fuel Type, Body Type  
  - Mileage (kmpl)  
  - Engine Capacity (cc)  
  - Age of the Car (years)  
  - Transmission Type (manual/automatic)  
  - City, Insurance, Kilometers Driven  
  - Number of Owners  

- **Real-time Price Prediction**: Get instant price predictions based on user input.  
- **Dynamic Dropdowns**: Model and variant options change based on the selected manufacturer for a smoother experience.  
- **Streamlit UI**: A user-friendly interface to interact with the car price prediction model.  

## **⚙️ Installation**

### **Prerequisites:**
- Python 3.x  
- Streamlit  
- scikit-learn  
- Matplotlib  
- Pandas  
- Numpy  
- Pillow (for image processing)

### **Steps:**
1. Clone the repository:  
   ```bash
   git clone https://github.com/Mugilan2004dbmy/Car-Dheko---Used-Car-Price-Prediction.git  
   cd Car-Dheko-Used-Car-Price-Prediction
   ```

2. Install the required dependencies:  
   ```bash
   pip install -r requirements.txt
   ```

3. Download the pre-trained model:  
   Ensure the `random_forest_model_with_preprocessor.pkl` (pre-trained Random Forest model with preprocessor) is in the project directory.

4. Run the basic functionality of the app:  
   ```bash
   streamlit run app.py
   ```

5. Run the enhanced version of the app with advanced features:  
   ```bash
   streamlit run app_final.py
   ```

## **🚀 Usage**

1. Start the app (`app_final.py` for full features) and open it in your browser.
2. In the **Car Specifications** section, input the following:
   - **Manufacturer**: Choose the car's manufacturer.
   - **Car Model**: Choose the model (filtered based on manufacturer).
   - **Variant**: Select the car’s variant.
   - **Fuel Type**: Choose between petrol, diesel, or other fuel types.
   - **Body Type**: Select the body type (SUV, Sedan, etc.).
   - **Mileage**: Enter fuel efficiency (kmpl).
   - **Engine**: Enter engine capacity (cc).
   - **Seats** and **Number of Cylinders** can also be specified.

3. In the **Other Details** section, enter:
   - **City**: Where the car is located.
   - **Insurance**: Select insurance status.
   - **Kilometers Driven**: Enter the total kilometers driven.
   - **Model Year**: Specify the car’s year of manufacture.
   - **Number of Owners**: Choose how many owners the car has had.

4. Click **Predict Price** to view the estimated price.
5. The predicted price will be displayed along with an explanation of how various features contributed to the price.

## **🧠 Model Training and Tuning**

The model used is a **Random Forest Regressor**, trained on historical car sales data.

### **Hyperparameter Tuning:**
Hyperparameters were optimized using **RandomizedSearchCV** to improve model accuracy, including:
- `n_estimators`: Number of trees in the forest.
- `max_depth`: Maximum depth of the trees.
- `min_samples_split`: Minimum samples required to split a node.
- `min_samples_leaf`: Minimum samples required for a leaf node.

### **Feature Engineering:**
Key features used include:
- Manufacturer, CarModel, Variant, FuelType, BodyType  
- Mileage (kmpl)  
- Engine Capacity (cc)  
- Age of Car (years)  
- Transmission Type (Manual/Automatic)  
- Insurance, Kilometers Driven, City  

The preprocessing pipeline ensures categorical and numerical features are handled correctly.

## **🎨 Examples**

Here are screenshots of the app interface:

### **Feature App**
![Base App](screenshots/screenshot1.png)

### **Basic App**
![Feature App](screenshots/screenshot2.png)

## **💬 Contributing**

We welcome contributions! To contribute:
1. Fork the repository.
2. Create a new branch for your feature (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -am 'Add a feature'`).
4. Push to your branch (`git push origin feature-branch`).
5. Create a pull request.
