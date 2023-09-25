# AB-Testing

## Task
To evaluate which version of the current "Interact" button performs best.

## Overview
The Library of Montana State University has a website that students use to find books and articles.

Below the library picture, there is a search bar and three big items: “Find”, “Request” and “Interact”. All three of them contain access to important information however, the Website Analytics show that the “Interact” button has, ironically, almost no interactions.

The MSU team  wants to run a 5-way AB Test. They would like to us to compare the performance of the original button "Interact", to new versions: "Learn", "Help", "Connect", "Services".

The way to measure how each one of the buttons perform is by click-through-rate or CTR. 

## Context
When assessing the effectiveness of the "Shop Now" button on an e-commerce website, the focus is on optimizing click-through rates due to visitors' clear intent to make a purchase. 

Conversely, evaluating the performance of a button like "Interact" on a library website requires considering that visitors may not always have a specific interest in what it offers. For instance, if a visitor is seeking a book and uses the "Find" function, they may not find the "Interact" button useful or relevant.

In addition to click-through rates, it's crucial to analyze the homepage return rate and drop-off rate on the library's website. This broader evaluation helps gauge whether visitors are finding the information they expect after interacting with a specific button.

## Challenge:
Plan, structure and execute a 5 way AB Test. 

## Approach
Hypothesis Testing:

* Explore the current data and result of UI/UX questionnaires available
* Calculate length of the AB test based on MDE and number of visitors
* Set up the 5 tests, length and the 5 versions (done for us)
* Explore raw data, CTR rates of all 5 versions (explore, clean, note anomalies)
* Form and record hypothesis (H0 & H1, metrics of interest, MDE, alpha and beta scores, test to use) 
* Categorical data, 5 versions - Chi-Square test
* Adjust for cumulated alpha error with Bonferroni correction

## Colab Files
In the "MSU Library" file imported the data, each button its own csv. All calculations are included. Drop-off and Homepage return rates were given by the MSU team. 

### Additional Notes:
The data was highly skewed; (10283 visits on "Interact" vs the others versions recieved visits in the 2000-3000 range). 
Therefore, after completing the calculations based on the requested parameters (CTR = visits / clicks). I reran the experiment at the end of the notebook under heading _"Chi-Square Test - CTR 2"_  where I defined CTR as elemnt of interest clicks / all clicks on the website. Ideally, the test should have been rerun, as it was *biased* from the beginning. 

#### I feel this adjusts for 2 factors:
* Someone might not actually need the "Interact" button - or any other version of it
* Less skewed than visits.

# Skills & Tools
1. Data Collection & Cleaning
2. Hypothesis Testing
3. AB Testing
4. Chi-Square Testing
5. Bonferroni Adjustment
