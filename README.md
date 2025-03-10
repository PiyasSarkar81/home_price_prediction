# Bengaluru House Price Prediction

This project aims to predict house prices in Bengaluru using various machine learning algorithms. The dataset used contains information about different properties in Bengaluru, including features like location, size, total square feet, number of bathrooms, and more.

## Project Structure

- `Model/bhp.ipynb`: Jupyter notebook containing the data analysis, feature engineering, and model building steps.
- `server/server.py`: Flask server to serve the model and provide predictions via API endpoints.
- `banglore_home_prices_model.pickle`: Serialized model file.
- `columns.json`: JSON file containing the data columns used in the model.

## How to Run

1. Clone the repository.
2. Install the required dependencies using `pip install -r requirements.txt`.
3. Run the Jupyter notebook `Model/bhp.ipynb` to understand the data analysis and model building process.
4. Start the Flask server by running `python server/server.py`.

## API Endpoints

- `/get_location_names`: Returns a list of location names used in the model.
- `/predict_home_price`: Predicts the house price based on the input features (total_sqft, location, bhk, bath).

## Usage

You can use the API endpoints to get predictions for house prices in Bengaluru. Below is an example of how to use the `/predict_home_price` endpoint:

```bash
curl -X POST http://127.0.0.1:5000/predict_home_price -d 'total_sqft=1000&location=Indira Nagar&bhk=2&bath=2'
```

## How to Use the Application

1. Open the `client/app.html` file in a web browser.
2. Enter the area in square feet in the "Area (Square Feet)" field.
3. Select the number of BHKs and bathrooms using the radio buttons.
4. Choose a location from the dropdown menu.
5. Click the "Estimate Price" button to get the estimated price.
6. The estimated price will be displayed below the button.

## License

This project is licensed under the MIT License.

