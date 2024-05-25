# Guardian-of-the-Web-Predicting-URL-Safety-with-Machine-Learning
Develop a robust machine learning model that accurately classifies user-provided URLs as either safe or unsafe. The project involves data preprocessing (including cleaning and feature extraction), model training, performance evaluation, and user-friendly interaction for real-time URL safety predictions.

### 1. Data Cleaning and Preprocessing
- Ensure that your dataset is clean and well-structured.
- Remove irrelevant features and handle missing values.
- Preprocess the URLs (e.g., tokenization, character encoding).

### 2. Feature Extraction
- Extract relevant features from the URLs.
- Consider features like domain length, presence of specific keywords, and URL length.

### 3. Model Training
- Split your dataset into training and validation sets.
- Train a binary classification model (e.g., logistic regression, decision trees, neural networks).
- Evaluate model performance using metrics like accuracy, precision, recall, F1-score, and AUC-ROC.

### 4. User Input and Prediction
- Receive user input (URL format).
- Preprocess the input (similar to training data).
- Pass the processed input through your trained model.
- Set a threshold to classify the URL as safe or unsafe based on predicted probabilities.

### 5. Save your model in pickle formate.
```python
#you must have to import pickle
import pickle
with open('model.pkl','wb') as file:
   pickle.dump(model_name,file)
#it will stored in current directory 
```


## Usage
1. **Preprocessing and Feature Extraction**:
   - Ensure that the input URL is preprocessed in the same way as during training.
   - Extract relevant features (e.g., domain length, keywords).

2. **Prediction**:
   - Use the trained model to predict the URL's safety.
   - If the predicted probability is above a threshold (e.g., 0.5), classify it as unsafe; otherwise, classify it as safe.

3. **Example Code**:
   ```python
   # Load your trained model (replace with actual model loading code)
   model = load_model("trained_model.h5")

   def predict_url_safety(input_url):
       # Preprocess input_url (similar to training data)
       processed_url = preprocess_url(input_url)

       # Make predictions
       prediction = model.predict(processed_url)
       if prediction > 0.5:
           return "Unsafe"
       else:
           return "Safe"

   # Example usage
   user_input_url = "https://example.com/malicious-page"
   result = predict_url_safety(user_input_url)
   print(f"URL is {result}")
   ```

## Conclusion
By following these steps, you can effectively predict whether a user-provided URL is safe or unsafe. Remember to keep your model updated and monitor its performance regularly.

**Note**: Replace placeholders (e.g., `"trained_model.h5"`, `preprocess_url()`) with actual code and filenames specific to your implementation.
