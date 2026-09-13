# Projects
This section documents my data science projects, research questions, and data stories I create throughout the semesters.

---
## Project 1

## 1. Defining the Problem
The main focus is to evaluate the reactions of the audience and find patterns across multiple movie genres using data from the TMDB API.

Furthermore, I want to look into one important question that I want to answer from this data: 
How does a movie's runtime correlate with its audience rating and how does this relationship remain consistent across different genres

Why is this question relevant? Well, this type of data can be really improtant for film studios, producers, and streaming platforms looking to optimize production budgets and find their ideal length of a film based on what movie genre they want to make to maximize audience satisfaction.

## 2. Data Description
This project relies on data extracted directly from The Movie Database (TMDB API). The unit of analysis is individual feature films.

**Key Variables Coceptualized and Operationalized**
* **Genre:** The category or style of the movie, measured by mapping TMDB's 'genre_ids' to their official string names via the TMDB Genre List API.
* **Audience Rating:** Audience enjoyment, measured by the 'vote_average' score (0-10).
* **Runtime:** The length of the movie, measured in minutes via the TMDB Movie Details API.
* **Vote Count:** The total number of audience members who rated the film, measured by the 'vote_count' field.

**Academic Context & References:**
1. Souza, T. L. D., Nishijima, M., & Fava, A. C. P. (2019). Do consumer and expert reviews affect the length of time a film is kept on screens in the USA? *Journal of Cultural Economics*, 43(1), 145-171.
2. McKenzie, J. (2023). The economics of movies (revisited): A survey of recent literature. *Journal of Economic Surveys*, 37(2), 480-525.
3. Sikdar, S., Kang, U., & O'Donovan, J. (2015). Statistical patterns in movie rating behavior. *PLOS ONE*, 10(8).

## 3. Data Cleaning and Preparation
To make sure the integrity of the analysis, several cleaning steps were executed using pandas:
1. **Handling Missing Values:** Any rows missing `runtime` or `vote_average` were dropped, as these are the core variables of the research question.
2. **Filtering Vote Counts:** Movies with fewer than 100 votes were removed. This trade-off reduces the overall dataset size but prevents obscure movies with a single 10/10 rating from artificially skewing the runtime-to-rating correlations.
3. **Primary Genre Extraction:** Because films often feature multiple overlapping genres, only the first (primary) `genre_id` was extracted to allow for clean categorical grouping when testing consistency across genres.

## 4 & 5. Visualizations, Insights, and Storytelling
To address how runtime impacts audience scores across genres, we must first establish a baseline. The bar chart reveals that audiences inherently rate certain genres (like Drama and Animation) higher on average than others (like Action or Horror).

Building on that baseline, the scatter plot examining runtime versus rating demonstrates how movie length influences these scores. The visualization shows a dense cluster of mid-rated films (6.5 to 7.5) spanning the 100 to 115-minute mark. While a longer runtime does not automatically guarantee a better rating, there is a visible trend: genres typically associated with longer runtimes (such as Drama) maintain their higher rating baseline, whereas genres like Science Fiction show massive variance, swinging from a 4.0 rating at shorter runtimes to an 8.6 at longer runtimes.

## 6. Limitations, Ethics, and Reflection
While TMDB offers a massive repository of data, several limitations exist:
* **Genre Simplification:** Operationalizing a film by only its *primary* genre strips away meaning. A multi-genre film categorized solely by its first tag masks its true appeal and may skew genre-specific correlation results.
* **Demographic Bias:** TMDB ratings are crowd-sourced from its specific user base. These ratings do not represent a true random sample of the global population.
* **Next Steps:** If given more time, I would run regression lines for each specific genre on the scatter plot to see if the correlation strength changes dramatically between categories.

## 7. Code and Transparency
* **GitHub Repository:** [Insert your GitHub URL here]
* **Data Source:** The Movie Database (TMDB) API
* **AI Usage Disclosure:** Generative AI was utilized strictly for reformatting / cocising my words, and for formatting my code + understanding certain elements to make sure they were used properly. All original ideas were made by me as well as all references come from previous material made in class on canvas or previous VS Code files.
