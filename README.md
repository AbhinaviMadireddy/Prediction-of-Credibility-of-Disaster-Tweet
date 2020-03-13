# Prediction-of-Credibility-of-Disaster-Tweet

Built a model using Ridge Classifier following extraction of features using Tf-Idf Transformer. Performed data cleaning of 10,000 records of tweets by deleting the re-tweets data, replacing words as per requirement and evaluated the model using cross-validation.

# Data Cleaning
 --> Deleted the re-tweets data which constitutes to duplicate data
 
 --> Used the replace_terms function that matches every word of tweets with specified Regular Expression and replaces the word if required.
     
   # Extraction of Features
   Extracted a vector of Features required to fit a model using Td-Idf transformer.(Observed a significant change in the efficiency of        the model implemented with use of Td-Idf transformer over Count Vectorizer).
     
   # Fit a Ridge Classifier to the extracted features and measured the efficiency with cross-validation.
   
     
     
    
    
