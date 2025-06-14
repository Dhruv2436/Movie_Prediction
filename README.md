#🎬 Movie Success Prediction using K-Nearest Neighbors (KNN)
    This project uses machine learning to predict movie success (Flop, Average, or Hit) based on IMDb ratings and various movie-related features such as duration, budget, and Facebook likes of cast and crew.

## 📁 Project Structure
    ## 📊 Dataset
    
    The dataset (`movie_metadata.csv`) contains information about movies, including:
    
    - `imdb_score`
    - `duration`
    - `gross`
    - `budget`
    - Facebook likes (actors, director, movie)
    - Number of reviews, voted users, posters, etc.

### Target Variable
    We categorize `imdb_score` into 3 bins:
    - `FLOP`: IMDb score between 1 and 3
    - `AVG`: IMDb score between 3 and 6
    - `HIT`: IMDb score between 6 and 10

This binned category becomes the **label** for prediction.

## 🧠 Model Used
We use the **K-Nearest Neighbors (KNN)** classifier from `scikit-learn` with:
- `n_neighbors = 3`

## 🛠️ Libraries

- `numpy`
- `pandas`
- `matplotlib`
- `scikit-learn`

## 🚀 How It Works
1. **Preprocess Data**:
   - Drop missing values
   - Bin IMDb scores into categories
2. **Train-Test Split**:
   - 70% training / 30% testing
3. **Train KNN Model**:
   - Fit on selected features
4. **Predict and Visualize**:
   - Display predictions, confusion matrix, classification report
   - Bar plots for success category distribution

## 📈 Visual Output

1. **Test Set Success Distribution**:
   - Shows how many movies in the test set fall into each category (`FLOP`, `AVG`, `HIT`)

2. **Entire Dataset Distribution**:
   - Shows how the dataset is skewed across categories

## 📋 Evaluation Metrics
The model outputs:
- **Confusion Matrix**: how well the model distinguishes classes
- **Classification Report**:
  - Precision, Recall, F1-score for each category

## 🧪 Sample Prediction
    Predicts success of a new movie based on example feature values:
    Predicted movie success for IMDb scores: ['AVG']
    pip install pandas scikit-learn matplotlib

🧾 Notes
    Be sure the movie_metadata.csv file is placed one level above your script directory.
    
    Update the path in your code accordingly:
    pd.read_csv("../movie_metadata.csv")
