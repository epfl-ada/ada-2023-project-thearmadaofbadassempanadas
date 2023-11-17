# Charting a path to cinematic success 

## Abstract

As a woman with a deep passion for cinema, I aspire to become a celebrated actress and make a lasting impact in the film industry. My journey, guided by strong values and ambition, takes a unique path through the enchanting world of cinema, each region sparkling with its own distinct characteristics. Accompanied by a skilled team of data analysts, I navigate the cinematic landscape like a treasure map, seeking fame and impact. My goals are twofold: achieving personal success and advocating for female representation and equal opportunities in cinema. We explore the diverse landscape of the world's film industries, from Hollywood's glamour to Europe's cultural heritage and the dynamic energy of Bollywood in Asia, seeking to pinpoint where the most promising prospects for wealth, achievement, and fellowship are found.

## Research Questions

In my quest to find out the ideal career path, I, together with my data analysis team, seek answers to these pivotal questions:
- How does gender and ethnicity representation vary across different film industries, and what role can I play in enhancing gender equality in my chosen region?
- What are the patterns of wealth and success in the global film industries, and which regions provide the most favorable environment for financial prosperity and passion in acting?
- How is the network of actors, directors, and industry players structured in various regions, and how does this influence individual success?

## Methods

**Part 1: Data exploration**
1. **Data cleaning:** TODO 
1. **Movie grouping:** Data exploration, Scrapping movies' country, Group by geographic area TODO
1. **First data exploration and visualization:** Study different axis using movies and characters metadata.
1. **NLP pipeline:** the plot summaries of each movie could be analyzed to gain further insights on each film industry. This process could be used as an additional tool for the different analysis axes of the project, by performing different types of text processing. We first use sentiment analysis using the stanza package to assign a sentiment score to each sentence (0 for negative, 1 for neutral, 2 for positive). Each plot summary is then a list of sentiment scores of each sentence, highlighting the global emotional tone. Stanza also allows to get word representations. Then, we will also extract more sophisticated emotional tones using the NRCLex package. We can also push further by using aspect-based sentiment analysis to get the sentiment score of specified topics, like female relative words, using aspect-based-sentiment-analysis package. This code has been run on google colab to take advantage of the free GPU running.
    
**Part 2: Data analysis to answer our scientific questions**
1. **Film revenue:** TODO
1. **Gender representation:** TODO
1. **Ethnicity:** TODO
1. **Linking between actors:** TODO

**Part 3: Generalization and story telling**
1. **Answer our questions** based on the results of analysis
2. **ML classification:** build a ML model to assign an actor to its best matching industry based on its features
3. **Comparison:** compare the results of manual and automatic analysis

## Proposed timeline

In order to start my carreer as soon as possible to enter the world of film industry, I fixed some milestones to my team:

| Week | Milestones |
| --- | --- |
| 9 | Data cleaning <br> Categorization of films by geographical areas <br> Initial analysis on project dimensions <br> P2 deliverable |
| 10 | <em>Team in vacation (Work on Homework 2)<em> |
| 11 | <em>Team in vacation (Deadline Homework 2)<em> |
| 12 | Completion of NLP pipeline <br> initiation of HTML website |
| 13 | Development of data story |
| 14 | Finalizing HTML <br> Repository cleanup |

## Organization within the team

To efficiently navigate my path to success in the film industry, our team roles are strategically distributed:

| Data Analyst | Tasks |
| --- | --- |
| Flore | Preprocessing (movie grouping) <br> Analysis of ethnicity in movies |
| Justine | Study of revenue across industries |
| Lola | Investigation of female representation |
| Chléa | Overseeing NLP pipeline <br> Crafting data story and README |
| Léon | Data cleaning and scrapping <br> Analysis of actor interconnection |

## Questions for TAs

TODO
