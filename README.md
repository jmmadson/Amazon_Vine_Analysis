# Amazon Vine Analysis of Musical Instruments

## Overview 
The purpose of this Amazon Vine Analysis was to analyze reviews from Amazon on Musical Instruments to confirm whether Amazon's paid review program, Vine, had a positive bias on the overall review results. To complete this analysis I took the musical instrument review data from storage on AWS, brought it into a DataFrame using Google Colab and PySpark, where I filtered the data down to focus on reviews with more than 20 votes, with 50% of those votes being "helpful votes". I further narrowed the dataframe to find the total number of reviews, total number of Five Star reviews and Five Star reviews by Paid (Vine) vs. UnPaid (Non-Vine) origin to help uncover if there was a bias. 

## Results
From my analysis I found the following: 
<ul>
<li>Of the 6,796 total reviews, 3,852 of them where Five Star reviews.</li>
<li>Of the 6,796 total reviews, there were 35 Vine Reviews and 6,761 Non-Vine reviews. </li>
<li>There were 21 Vine Five Star reviews and 3,831 Non-Vine Five Star Reviews as shown below in Example A.</li>
<li>Vine reviews accounted for 0.5% of Five Star reviews, while Non-Vine reviews accounted for 99.5% of all Five Star reviews as shown below in Example B.</li>
</ul>

<strong>Example A. Five Star Review Counts for Vine and Non-Vine Reviews</strong>
![Example A. Total Vine & Non Vine Reviews](https://github.com/jmmadson/Amazon_Vine_Analysis/blob/main/Images/Paid_vs_Unpaid%20Count.png?raw=true)
<br> 

<strong>Example B. Five Star Review % for Vine and Non-Vine Reviews</strong>
![Example B. Vine & Non Vine Review %](https://github.com/jmmadson/Amazon_Vine_Analysis/blob/main/Images/Paid_Vs_UnPaid.png?raw=true)
<br>
## Summary

For the purposes of this analysis, assuming that a Five Star review is the indicator for a positive bias on the dataset, the number of paid Five Star reviews is minuscule, so the data is not skewed by positive paid (Vine) reviews. That said, when you look at the number of Five Star Vine reviews in my data set (21) divided by the number of total Vine reviews (35), you can see that 60% of the reviews that are paid, were Five Star reviews. So while it does not affect the total reviews for Musical Instruments due to volume, there is a positive bias in the Vine Reviews for Musical Instruments based on the reviews analyzed. 
![Vine Review %](https://github.com/jmmadson/Amazon_Vine_Analysis/blob/main/Images/Positive_Bias.png?raw=true)

To dig into this further, I would like to rerun the previous analysis, including both 4 and 5 star ratings as positive indicators, and additionally try the analysis with different and larger data sets to fully see the impact the positive bias may have across products.

