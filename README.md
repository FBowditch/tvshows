# Shake It Off
## The critics don't know what the people want
We analyze Nielsen ratings and Rotten Tomatoes scores to find that critic and
audience reviews don't have much to do with what people actually watch.

## Contributors
 - Findlay Bowditch ([github](https://github.com/fbowditch))
 - Ravi Charan ([github](https://github.com/rcharan/))

## Background
This is our Flatiron School (NYC Data Science) Module 1 project

See the presentation and conclusions on [Google Slides](https://docs.google.com/presentation/d/1dP1xmHtrPHWAQQHPZnXCRq4pj1hd0MhsZ-TQ6PKXw7k/edit?usp=sharing) or view the pdf shake-it-off.pdf in our repo.

## Project Purpose and Description
 - The purpose of this project was to provide actionable insights to a
 hypothetical large company looking to enter the streaming wars (i.e. compete with
  Amazon Prime Video, Netflix, Hulu, Disney+, Apple TV+, etc.)
 - An ancillary purpose was to demonstrate and practice our new-found skills
 in web scraping, API usage, SQL, pandas, visualization (matplotlib/seaborn), and creation of ETL pipelines.
 - Data:
   1. Nielsen Ratings (national overnights 18&ndash;49) on a daily basis for broadcast primetime and the top 25 cable shows. Scraped from [TV By the Numbers](https://tvbythenumbers.zap2it.com). Available back to 2015
   2. Rotten Tomatoes audience and critics scores for matched TV shows (766)
   3. A list of Netflix and Amazon shows (via Wikipedia: [Netflix](https://en.wikipedia.org/wiki/List_of_original_programs_distributed_by_Netflix), [Amazon](https://en.wikipedia.org/wiki/List_of_original_programs_distributed_by_Amazon))
 - Tools (all in Python):
   1. BeautifulSoup
   1. pandas
   1. SQLAlchemy
   1. MySQL Server on AWS RDS
   1. Seaborn/Matplotlib

![Screenshot](https://github.com/FBowditch/tvshows/Chart_Plots/Workflow.png)

## How to use this repo

### Extract
 - data-extraction.ipynb does the extraction (use this).
 - tv_by_the_numbers.py scrapes TV By the Numbers. It also contains several scraping utilities
 - tv-show-extra-finding.ipynb works to improve matching to TV By the Numbers shows to Rotten Tomatoes
 - nflix_amaz_shows.ipynb loads the wikipedia data from a stored csv
 - rotten_tomatoes.py provides Rotten Tomatoes scraping

### Transform (and load)
 - transform-and-load.ipynb joins the appropriate tables and does data cleaning

### Analysis
 - analysis.ipynb in the top level directory
