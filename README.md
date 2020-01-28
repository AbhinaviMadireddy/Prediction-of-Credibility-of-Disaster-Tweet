# Prediction-of-Credibility-of-Disaster-Tweet

Built a model using Ridge Classifier following extraction of features using Tf-Idf Transformer. Performed data cleaning of 10,000 records of tweets by deleting the re-tweets data, replacing words as per requirement and evaluated the model using cross-validation.

# Data Cleaning
 --> Deleted the re-tweets data which constitutes to duplicate data
 
 --> Used the following function to replace words that matches every word of tweets with specified Regular Expression and replaces the word if required.
 
 def replace_terms(data):
    for word in data.split():
        word=word.lower()
        value1=re.match(".*@.*",word)
        if value1:
            data = re.sub("@","@ ",data)
        value2=re.match(".*:.*",word)
        if value2:
            data = re.sub(":"," : ",data)
        value3=re.match(".*#.*",word)
        if value3:
            data= re.sub("#","# ",data)
        value4=re.match(".*/.*",word)
        if value4:
            data= re.sub("/"," / ",data)
        value5=re.match(".*_.*",word)
        if value5:
            data= re.sub("_"," _ ",data)
        value6=re.match(".*[0-9]+[a-zA-Z][a-zA-Z]",word)
        if value6:
            index=0
            for i in range(len(word)):
                if word[i] not in ["0","1","2","3","4","5","6","7","8","9"]:
                    index=i
                    break
            word1=word[:index]
            data=re.sub(re.escape(word)," "+word1+" ",data)
     return data
     
   # Extraction of Features
     
     Extracted a vector of Features required to fit a model using Td-Idf transformer.(Observed a significant change in the efficiency of  the model implemented with use of Td-Idf transformer over Count Vectorizer).
     
   # Fit a Ridge Classifier to the extracted features and measured the efficiency with cross-validation.
     
     
    
    
