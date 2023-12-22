# Charting a path to cinematic success 

Here is the link to our [storytelling website](https://chlea38.github.io/ada-website).

## Abstract

As a woman with a deep passion for cinema, I aspire to become a celebrated actress and make a lasting impact in the film industry. My journey, guided by strong values and ambition, takes a unique path through the enchanting world of cinema, each region sparkling with its own distinct characteristics. Accompanied by a skilled team of data analysts, I navigate the cinematic landscape like a treasure map, seeking fame and impact. My goals are twofold: achieving personal success and advocating for female representation and equal opportunities in cinema. We explore the diverse landscape of the world's film industries, from Hollywood's glamour to Europe's cultural heritage and the dynamic energy of Bollywood in Asia, seeking to pinpoint where the most promising prospects for wealth, achievement, and fellowship are found.

## Research Questions

In my quest to find out the ideal career path, I, together with my data analysis team, seek answers to these pivotal questions:
- How does gender and ethnicity representation vary across different film industries, and what role can I play in enhancing gender equality in my chosen region?
- What are the patterns of wealth and success in the global film industries, and which regions provide the most favorable environment for financial prosperity and passion in acting?
- How is the network of actors, directors, and industry players structured in various regions, and how does this influence individual success?

## Methods

### **Step 1: Data cleaning**
1. **Data exploration for countries:**

The overarching aim of this step is to conduct a comparative analysis of the film industries from four globally distinct regions:
- *East Asia:* Japan, Hong Kong, China, South Korea, Taiwan
- *Western Europe:* United Kingdom, France, Italy, Germany, Spain, West Germany, Belgium, German Democratic Republic, Ireland, Switzerland, Austria, England, Luxembourg, Portugal
- *Northern America:* United States of America, Canada
- *India:* India and Pakistan
  
The main activity is to categorize each film by its corresponding global region. During our initial examination of the movie database, we noticed that some films were connected to multiple countries. Our approach to resolve this included:
- Assigning films linked to a single country to the appropriate global region. Films not fitting into our specified regions were excluded.
- For films connected to several countries within the same region, we allocated them to that specific global area.
- In cases where films were linked to countries across different regions, we utilized the Wikipedia API to obtain the necessary details.

This process allowed us to effectively sort movies into the four major world regions, setting the stage for subsequent in-depth analysis and comparisons.

2. **Country information extraction**

Our task focused on determining the actual production countries of films in the dataset, a necessity due to the lack of clarity in the 'countries' column. We utilized the Wikipedia API for this purpose. Given that over 14,000 movies lacked clear country identification, this endeavor required more than 8 hours of dedicated effort. The primary aim was to retain these films in our dataset, avoiding their exclusion while we conduct other forms of data cleaning.

3. **Plot summary extraction:**

The CMU movie summary corpus contains a supplement, containing Standford CoreNLP-processed summaries. In order to include informations from the summaries into our analysis, we need to extract those data. The raw supplement dataset is composed of a zipped folder for each movie, containing an XML file with the results of the NLP analysis. We first extract the zipped folder, and then move the xml files in a centralized folder. Due to the large size of this supplementary dataset, we decided not to add these files to the repository. Therefore, to run the script you need to add the folder containing all the zipped folders at the level of the cloned repository, and then to run the part 1.3. to extract all files.
    
### **Step 2: Data exploration and visualization**

1. **Film revenue:**

We looked at the proportion of missing data over the different geographical areas, and over the years. This led us to discard this feature from our analysis given the lack of data.

2. **Movie genres:**

Once we checked that the quantity of missing data is minime, we removed it. We then had a quick overview of the distribution of movie genres across the different geographical areas. The dataset offered a rich array of movie genres, including highly specific and distinct ones. The initial movie genres were clustered into broader categories, covering multiple sub-genres, with the help of pre-existing word embeddings. Additionally, movies accounting for less than 2% of the total collection were consolidated under an *Others* category to simplify the representation of this huge variety of genres. 

3. **Gender representation:**

Based on the characters document, we started by cleaning the data from NaN values for relevant features only, as to avoid over-sanitizing our data. We then completed the data with the geographic region and year of release from the movies dataset. Finally, we subsetted the data by gender, allowing us to compare their entries but also their repartition over time and regions with plots, to get a first idea.  

4. **Ethnicity:**

First we identified the proportion of missing data for actor ethnicities in our four different regions. We observe a large proportion of missing values, but due to resource constraints, we decided to remove them instead of attempting to scrape the absent actor ethnicities.  After having retrieved the ethnicity labels corresponding to the ethnicity Freebase ID we visualized how the ethnicity diversity evolves across the different regions of the world.

5. **NLP:**

This part is separated into two methods. The first is to use the supplementary dataset by parsing the xml files containing the results of the CoreNLP analysis. This allows to extract word features, dependencies between words and coreference within the text.
The second part aims to apply sentiment analysis to the summaries. This could be useful for the previous analyses, for exemple to extract sentiment of female-related terms using aspect-based sentiment analysis. From these two methods, we built an analysis pipeline to extract information based on a defined vocabulary, here female-related vocabulary, and compare the results from the 4 areas.

### **Step 3: Analysis and industry benchmarking**

1. **Comparison of film industries:**

Our analysis aims to distill key trends in the film industry using statistical and graphical methods. We'll focus on understanding the elements driving success in various regions. Key components of our approach include:
- Diversity Mapping: Assessing gender and ethnicity within the industry's actors and crew to understand the representation landscape in different film markets.
- Genre analysis: Examine the intrinsic traits of the film industry within different geographic regions. The aim is to pinpoint the most promising genre for employment within each region by uncovering the predominant genre, which holds the largest share of movies. Additionally, we delve into the evolution of genres over time, examining whether industry trends have influenced the prevalence of these top genres.
- Demographic breakdown of lead roles within a prevalent genre:  Focusing on drama movies, we explore potential variations in gender representation and actresses' ages across these regions.

2. **Actor network analysis:**

An additional aspect involves mapping the connections between actors using graphical representations. This will help us understand the influence of actors in the industry, particularly those involved in high-grossing films. We'll also examine actor clusters who have appeared together in films. This stage intends to explore whether the trends we've observed align with the networks of influential actors.

3. **Forecasting optimal industry for actors:**

To push further our project of charting a path to cinematic success, we propose to build a machine learning model to assign an actor to its best matching industry based on its wishes and personnal features.

## Proposed timeline

In order to start my carreer as soon as possible to enter the world of film industry, I fixed some milestones to my team:

| Week | Milestones |
| --- | --- |
| 9 | Data cleaning <br> Categorization of films by geographical areas <br> Initial analysis on project dimensions <br> Exploration of NLP for summaries <br> P2 deliverable |
| 10 | <em>Team in vacation (Work on Homework 2)<em> |
| 11 | <em>Team in vacation (Deadline Homework 2)<em> |
| 12 | Completion of NLP pipeline <br> Continue analyses on the different projet dimensions <br> Implementation of the ML model <br> Initiation of HTML website |
| 13 | Finish data analysis <br> Results analysis <br> Development of data story |
| 14 | Finalizing HTML <br> Repository cleanup |

## Organization within the team

To efficiently navigate my path to success in the film industry, our team roles are strategically distributed:

| Data Analyst | Tasks |
| --- | --- |
| Flore | Preprocessing (movie grouping) <br> Analysis of ethnicity in movies <br> Predictive model |
| Justine | Study of revenue and genres across industries |
| Lola | Investigation of female representation |
| Chléa | Extracting summaries <br> Building NLP pipeline <br> Crafting data story and README |
| Léon | Data cleaning and scrapping <br> Analysis of actor interconnection <br> Website development |
