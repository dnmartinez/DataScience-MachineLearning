Twitter project
* Due to the current pandemic, Krispy Kreme tried encouraging people to get vaccinated in exchange of free doughnuts. In this project I tried to determine if people thought this to be a good/bad idea based on their post's sentiment. 
* The tweepy_streamer file  retrieves twits with the krispykreme or KrispyKreme hastags froma specified date rage. 
* The TwitterSentiment file analyzes the sentiment. First, the data is loaded into an RDD and several new line and tab characters are removed to avoid the input of a certain cell to fall into another cell. Then it is turned into a DF and the data is cleaned using regular expressions(removing '#', emojies, '@', 'https?', new lines). I created user defined functions to apply the polarity and subjectivity functions to every row of my DataFrame. Results were graphed for comparison.

Loan project
* Using Spark's MlLib, I created a Cross Validation model to determine if a person should be approved for a loan
* I read in my data and tried to determine if it had any Null values. If so, I wanted to see what percentage of my data I would be deleting to have an idea of how much it would affect my future calculations. Only 21% of the data was deleted. 
* I identified my independent variables and dependent variable (Loan_Status). 
* Next, I formatted and transformed my dataframe using a StringIndexer, this would allow me to map a binary number to the loan status (my dependent variable). I did the same for the independent variables. The string_to_numeric_cols() function determines if the data type of the input columns is of StringType. If that is the case, then StringIndexer will be applied to give the column a numeric value
* I treated the data for skewness to avoid any mistakes/errors or poor performance in my Linear Regression model. 
* The DataFrame was later vectorized using VectorAssembler. The data was scaled to avoid any variances in range.
* The training and testing data was obtained using randomSplit of 70% for training and 30% for testing.
* Finally a confusion matrix was created
