## Appartment Building Evaluation

This project predicts apartment **overall ratings** from apartment review data using:
- **Nearest Neighbour**
- **Linear Regression**

It includes simple abstractions for apartment data, CSV loading utilities, model implementations, and a test script.

## Project Structure

- `abstractions.py`: Defines `Review` and `ApartmentBuilding`.
- `data.py`: Loads apartment data from CSV files in `datafolder/`.
- `classifiers.py`: Implements:
  - `NearestNeighbour`
  - `LinearRegression`
  - `calculate_mse`
- `testing.py`: Runs assertion-based tests for abstractions and models.
- `datafolder/apartments.csv`: Training dataset.
- `datafolder/testset.csv`: Testing dataset.

## Requirements

- Python 3.10+
- `matplotlib`

Install dependency:

```bash
pip install matplotlib
```

## Run the Project

Run model training, prediction, MSE output, and plots:

```bash
python classifiers.py
```

What this does:
- Trains linear regression on `APARTMENT_DATA`
- Predicts ratings on `TESTING_DATA`
- Prints regression MSE
- Shows regression scatter/line plots
- Runs nearest-neighbour predictions and prints MSE
- Shows nearest-neighbour plots

## Run Tests

Run the testing checks:

```bash
python testing.py
```

Run doctests in modules:

```bash
python abstractions.py
python classifiers.py
```

## Notes

- Data is loaded relative to the project root using `DATA_DIRECTORY = 'datafolder/'`.
- The current implementation in `calculate_mse` compares predictions against cosmetic ratings.
