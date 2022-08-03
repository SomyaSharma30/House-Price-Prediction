# House-Price-Prediction
Housing Price Prediction 
Using Random Forest Regression


Data set source: Kaggle

Data Preprocessing:

Data preprocessing is an important aspect of Machine Learning. It improves data quality which accelerates the accuracy, consistency, interpretability of our preprocessed data.
Steps involved in data preprocessing 

Data Cleaning: to remove noise and inconsistent data
Data Integration: where multiple data sources may be combined
Data selection: where data relevant to the analysis task are retrieved from the databases
Data Transformation: where data are transformed and consolidated into forms appropriate for applying machine learning algorithms

For the given Data Set:
It has a total of 21 attributes
     Suburb         
    Address
    Rooms    
    Type  
    Price 
    Method          
    SellerG        
    Date           
    Distance       
    Postcode       
   Bedroom2       
   Bathroom
   Car
   Landsize  
   BuildingArea  
   YearBuilt   
   CouncilArea    
   Lattitude      
   Longtitude    
   Regionname     
   Propertycount

In this dataset Car, YearBuilt, Council Area and Building are having some missing values
We fill the null values of the car attribute with zero
Year Built with mode
Council Area with Mode
Building area with Median 
We split the date into day, month and year for encoding it
In the address attribute, we extract the street name for model training

After that, we use Feature Engineering to find the best attribute for the best accuracy
We used the following attributes for the best accuracy 
Rooms
Type
Distance
Postcode
Landsize
BuildingArea
Longitude

After taking care of Data  integration, selection, and cleaning, the next step is Encoding our data 
We encode all the data using LabelEncoder() and Frequency Encoder from sklearn.preprocessing package
As Machine learning models require all input and output variables to be numeric, Encoding is an important step of data preprocessing


Training and Testing of the model 

We split data into two parts Train , Test
Then we use Random Forest Regressor on our preprocessed data

Random Forest Regression is a supervised learning algorithm that uses the ensemble learning method for regression. A Random Forest operates by constructing several decision trees during training time and outputting the mean of the classes as the prediction of all the trees


Then we fit the model using train set and check  their accuracy on the test set
 The final accuracy after testing the model is Random Forest Regressor - 82%

