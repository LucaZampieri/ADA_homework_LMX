# ADA Final Exam

## Deadline
Thursday February 02, 2017 at 11:15AM

## Important Notes
* Make sure you upload your iPython Notebook [with this form](https://script.google.com/macros/s/AKfycbxOi0MpR3WnGXrXjx85Q5W7ENteJI3gpD4_VL3zfZaX3CHnCDQ/exec) at the end of the exam, with all the cells already evaluated.
* Don't forget to add a textual description of your thought process, the assumptions you made, and the solution
you plan to implement!
* Please write all your comments in English, and use meaningful variable names in your code.
* As we have seen during the semester, data science is all about multiple iterations on the same dataset.
Do not obsess over small details at the beginning, and try to complete as many tasks as possible during the first 2 hours. 
Then, go back to the obtained results, write meaningful comments, and debug your code if you have found any glaring mistake.
* Remember, this is not a homework assignment -- **no teamwork allowed!**

## Goal
Today you will wear the hat of a data scientist who studies the Social Media presence of the two
major Swiss universities: EPFL and ETHZ. You will be given multiple tasks, ranging from data analysis
to machine learning, all aimed at spotting key differences between the two universities.

## Data Description
In this repository you can find two `.json` files containing the full Twitter history of the 
[EPFL_en](https://twitter.com/epfl_en) and [ETH_en](https://twitter.com/eth_en) accounts.
On the Twitter developers site you can read a full description of the [Tweet objects](https://dev.twitter.com/overview/api/tweets)
contained in the files. We recommend you to read carefully the documentation, in order to understand how useful each attribute could be for the assigned tasks.
Load the two files into Pandas dataframes, and then generate two additional dataframes filtered by `id % 10 == LAST_DIGIT_OF_YOUR_SCIPER_NUMBER`.
Whenever asked, perform the task on both the full dataframes and the downsampled ones, discussing what is the impact of the downsampling (if any).

## Tasks
1. Perform **data wrangling** as you see fit on *both the full and downsampled dataframes*, justifying your choices.

2. By means of **descriptive statistics and plots**, show the different volume of engagement (e.g., number of favorites and retweets) that the accounts generate.
Compute the results per year (to highlight the growth trends), per month (to figure out if the accounts follow the academic year), and per hour of the day (to
find out if tweets posted at a certain hour get more attention). Similarly, break down the results per hashtag (e.g., #EPFLisAwesome) -- are there hashtags that
are used more often than others, and that obtain more engagement than others?

3. Train a **regressor** (*both on the full and downsampled dataframes*) to predict how many retweets a certain Tweet will get. You are allowed to use as features
only the attributes in the JSON objects (and any derivative that you can build locally) -- you are not allowed to download additional data from the Internet
to boost your model. Discuss the obtained results, explain the performance on the downsampled dataframes, and briefly describe what additional features you
would have used if you had access to the full Twitter API.

  *HINT*: for a more powerful model, consider time (and how the audience of the accounts grew throughout the years...)

4. Find the **topics** that are covered most of the time by the two Twitter accounts (*both on the full and downsampled dataframes*). You can run topic modeling and/or
implement your own NLP pipeline. Do the topics change significantly over time? Is there an overlap with the hashtags used in the tweets?

  *HINT*: clustering Tweets by some features (e.g., hashtags) will give you better results with topic modeling.
