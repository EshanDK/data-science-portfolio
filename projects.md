# Projects
This section documents my data science projects, research questions, and data stories I create throughout the semesters.

---
## Project 1

## 1. Defining the Problem
The main focus is to evaluate the reactions of the audience and find patterns across multiple movie genres using data from the TMDB API.

Furthermore, I want to look into one important question that I want to answer from this data: 
**How does a movie's runtime correlate with its audience rating and how does this relationship remain consistent across different genres**

Why is this question relevent? Well, this type of data can be really improtant for film studios, producers, and streaming platforms looking to optimize production budgets and find their ideal length of a film based on what movie genre they want to make to maxmize audience satisfaction.

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
