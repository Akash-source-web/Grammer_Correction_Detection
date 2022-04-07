# Grammer_Correction_Detection
  ### Business Problem
   Check if the sentence is Grammatically correct: 
   Please use any pre-trained model or use text from open datasets.
   Once done, please evaluate the English Grammar in the text column of the below dataset.
   
 ### Solution
   In order to solve the problem I used a Pre-Build model named "GramFormer".
   This model take the input as a text and check the each statement that is their any grammetical 
   mistake are their or not and if it found so it will correct it and display you the output as a 
   correct sentence.
   
 ### Pre-Processing:
   Befoure passing the data I need to do some Pre processing that this model only take the text as a
   input so we need only the text column so I need to drop all column which do not contain any text.
      
        df=df.drop(['star','app_id','reviewDate'],axis=1)
        
 ### Model Building:
   In order to build the model we need some library to import i.e.
   import torch
   from gramformer import Gramformer
   import pandas as pd
   import numpy as np

   even befour importing these library first we need to pull the "GramFormer" model from GitHub
   to our local machine.

    !pip install -U git+https://github.com/PrithivirajDamodaran/Gramformer.git -q

   After installing this it take some time we import all the libraries.
   Now read the CSV file and do preprocessing and then give it to the model after the model output
   store the whole output into a DataFrame becouse this model did note store the output so we need to
   store it sepratly and then you can download the output file.

 ### Deployment:
   I use Streamlit to deploy the Project.
   This app take a CSV file as a input and give you the output which you can download.
   
 ##### Some of the Screen Shoots are attached below:


 ### Quetions:
   Q.Write about any difficult problem that you solved. 
    (According to us difficult - is something which 90% of people would have only 10% probability in getting a similarly good solution). 
    
   A.For me the most diffcult problem is the grammer check problem beacouse it very diffcult to 
     make a raw model for the grammer detection and correction and in order to search this I go through
     the internet and YouTube as well but I did not find any one who give me any raw model to check
     and correct the grammer of given text. After serching loat of time I found a github page with a
     Pre-build model which check the grammer and display the corrected text and also their are only few
     video on YouTube also. So, for me it is the difficult problem which take 3 days to me for only 
     finding the model.
     
   Q.Formally, a vector space V' is a subspace of a vector space V if
     V' is a vector space
     every element of V′ is also an element of V.
     Note that ordered pairs of real numbers (a,b) a,b∈R form a vector space V. Which of the following is a subspace of V?
     The set of pairs (a, a + 1) for all real a
     The set of pairs (a, b) for all real a ≥ b
     The set of pairs (a, 2a) for all real a
     The set of pairs (a, b) for all non-negative real a,b
     
   A.The set of pairs (a, b) for all real a ≥ b

