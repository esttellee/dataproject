# Description of project : Predicting Movie Ratings Based on Metadata and Award-winning Personnel

This project aims to predict movie ratings using metadata scraped from the Internet Movie Database (IMDB). The factors considered in the prediction model include the movie's genre, whether the director has won a Golden Globe, and the presence of famous actors in the cast.

## Prerequisites

The project is implemented in Python and requires the following libraries:

- BeautifulSoup
- Requests
- Pandas
- NumPy
- Scikit-learn

Ensure that these are installed in your Python environment before running the project.

## Project Features
- Extracting data of upcoming movies from the IMDb page.
- Scrapping movie attributes such as title, genre, director, and actors.
- Training a linear regression model to predict the movie ratings.
- Evaluating the model on a test dataset.
- Predicting the rating for upcoming movies.




## Building and Running the Assignment

1. **Clone the Repository:** Clone this GitHub repository on your local machine. You can do this using the following command on your terminal (you should have Git installed):
    ```
    git clone  https://github.com/esttellee/dataprojectipynb
    ```
2. **Install Python:** This project requires Python 3.x. If it is not installed on your system, you can download it from the official Python website (https://www.python.org/downloads/).

3. **Set up the Python Environment:** Navigate to the project directory and create a virtual environment.  Open a command prompt or terminal and execute the following commands:

    ```
    cd /path/to/project/directory
    python -m venv env
    ```
    
4. **Activate Virtual Environment:** Activate the virtual environment. Depending on your operating system, use the appropriate command:

    - On Windows:
    ```
    .\env\Scripts\activate
    ```
    - On macOS and Linux:
    ```
    source env/bin/activate
    ```
  
5. **Install Required Libraries:** Install the required Python libraries see in the prerequisites, If any of these libraries are missing, you can install them using the following command:

pip install beautifulsoup4 requests pandas numpy scikit-learn

6. **Understanding the Python Code:** 
   
   The provided Python script is designed to scrape data from the IMDb Top 250 movies webpage as well as from Allocine's most viewed actors and Golden Globe winners pages. The collected data includes movie titles, genres, directors, and actors. The script further analyzes this data to identify commonalities between well-known actors and Golden Globe-winning directors.

   The script can be broken down into the following key components:

    - Importation of necessary libraries (BeautifulSoup, requests, pprint, urlopen from urllib.request, and pandas).
    
    - Initial setup and scraping from IMDb's Top 250 movies page.
    
    - Scraping from Allocine's most viewed actors pages to get a list of well-known actors.
    
    - Scraping from Allocine's Golden Globe winners page to get a list of directors who have won a Golden Globe.
    
    - For each movie from IMDb's Top 250 page, the script visits the individual movie page to scrape additional data. This includes the movie's genre, director, and actors. 
    
    - Finally, the script creates a pandas DataFrame to store all the scraped data and prints it out.



## Additional Instructions:
Depending on the functionality you want to test, you can uncomment and run the specific code blocks related to data visualization, modeling, or specific URLs.

Remember to deactivate the virtual environment once you're done by running the command `deactivate`.


## Data

The data used in this project is scraped from the [IMDB Calendar](https://www.imdb.com/calendar/?ref_=rlm&region=BE&type=MOVIE). The information extracted includes movie titles, year, genres, director names, and cast lists. The directors are cross-referenced with a list of Golden Globe winners to predict the movie's potential success and the actors are cross-refeenced with a list of best actors provided by allocine website. 

## Methodology

The project uses a Linear Regression model trained on encoded movie data. The data encoding process involves Label Encoding for genre and One-Hot Encoding for director and actors' award-winning status. The model is evaluated using the mean squared error metric.

## Results

After processing the movie data and training the model, you can make predictions on new or upcoming movies. The output will be a dataframe containing the movie titles and their predicted ratings. Example:

```python
print(df_sorties[['title', 'predicted_rating']])
```



