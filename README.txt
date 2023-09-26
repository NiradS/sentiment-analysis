Hello,

Here you will find the details of this project (purpose, process, technologies used, etc.)

Purpose: The purpose of this project was to build a sentiment analyzing machine learning model, specifically for movies.

Process: The project is split into 3 parts:
            - A Web Scraper 
            - Data (created by Scraper)
            - A Machine Learning Model
            
            Web Scraper:
            - Selenium
            - Web Driver
            - HTML/CSS and Developer Tools Knowledge
            
            
            There were no publicly available recent data sets that contained a large volume of movie reviews and ratings. 
            As such, I created a Web Scraper to solve this solution and create a dataset tailored to the needs of this machine 
            learning model.
            The Web Scraper scrapes 50 pages of reviews and ratings from rotten tomatoes for any movie. The list of movies can be 
            user specified OR it can also be scraped from trending movies from IMDb (that scraper has not been included in this folder).
            ***NOTE***: This Scraper ran with built in delays between each page of reviews to prevent overloading of Rotten Tomatoes server.
            
            
            Data:
            - Reviews
            - Ratings
            
            The majority of the reviews are in English and as such, the Natural Language Processing Libraries are tailored towards
            English. However, there are non-english reviews as well, that can be removed during the pre-processing stage. (For my project
            I have not removed these reviews to further test my model in a "real world" environment)
            
            During the pre-processing stage for model training, the reviews are categorized as positive (4 stars and above) 
            or negative (2 stars and below).   
            Any reviews in between these two categories are removed. This aids in model clarity. 
            
            Machine Learning Model:
            - Python
            - Natural Language Processing, NLTK/PUNKT
            - Pandas, Numpy 
            - sckit-learn
            
            
            The Machine Learning model was fed the post-processed training data and trained with a split of the data (the split is randomly
            generated, but for reproductability reasons, the random seed is pre-set). 
            Then the Machine Learning model is tested against the test split and a confusion matrix is displayed to visualize
            True Negatives, True Positives, False Negatives, and False Positives. 
            
            Then the Machine Learning model is tested against the original data-set (the one which contains mixed 2.5,3, and 3.5 star
            reviews)
            
Technologies Used:
    - Web Scraping 
    - Selenium/Automated Browser Tools
    - Web Driver
    - HTML/CSS and Browser Developer Tools
    - Data Pre-Processing
    - Python, Pandas, Numpy
    - Machine Learning, Natural Language Processing, Sentiment Analysis
    
Additional Notes :
    - The Machine Learning Model's accuray relies entirely on the data is fed. For this reason, it is important that the Model 
    receives   large data that is both marked as positive and negative. If the Model is only fed popular, well-rated movies, it 
    will return many false positives and be of no use. 
    - The sentiment analysis model was greatly inspired by Data Camp. 
            