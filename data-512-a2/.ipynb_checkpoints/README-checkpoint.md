# Data 512 A2: Bias in Data

## Overview
In this assignment I perform two separate analysis on three different datasets created from the Wikipedia Talk Corpus. Each dataset contains comments made by Wikipedia editors. Crowd-workers from Crowdflower were hired to annotate these comments based on three kinds of hostile speech: "toxicity", "aggression", and "personal attack". In performing these two analyses, I hope to uncover some biases that may exist in these datasets.

## Data
This data comes from the Wikipedia Talk Corpus and can be downloaded from [Figshare](https://figshare.com/projects/Wikipedia_Talk/16731)

More information about the project can be found [here](https://meta.wikimedia.org/wiki/Research:Detox)

There are three different sets of data - one for each type of hostile speech. Descriptions of the data can be found [here](https://meta.wikimedia.org/wiki/Research:Detox/Data_Release)

The data exists here in three separate folders. The toxicity folder contains the toxicity datasets, the aggression folder contains the aggression datasets, and the attack folder contains the personal attacks datasets. Each folder has three separate data files. One of these files contains the annotations, one of of them contains the comments, and the last one contains Crowdflower worker demographic data.

The CSV formatted data used to generate my visualizations can be found in the output_data folder.

# Analysis
My first analysis looks at the crowd-worker data for the toxicity dataset. I did additional research on demographic information for Wikipedia editors and tried to compare that to the crowdworkers. Much of that additonal information can be found [here](https://en.wikipedia.org/wiki/Wikipedia:Wikipedians) and [here](https://en.wikipedia.org/wiki/Wikipedia:Who_writes_Wikipedia%3F#:~:text=28%25%20editors%20are%20aged%2040%2B.&text=59%25%20of%20the%20editors%20are%20aged%2017%20to%2040.&text=The%20English%20Wikipedia%20currently%20has,contributors%20participate%20in%20community%20discussions.). An example of one of the visualizations I generated from looking at age data for crowd-workers can be seen here:

![age distribution for crowd-workers](./visuals/toxicity_age_dist.png)

My second analysis looks into the words that are most common in comments labeled as "toxic", "aggression", or "attack". A visualization generated from this analysis can be seen here:

![toxicity word frequency](./visuals/toxicity_word_freqency.png)

All visualizations generated can be found in the visuals folder.

