# Datasets of DA project for Digitization at VU
This repository contains all used datasets for a small DA project for <i>Digitization: From Object To Data</i> at the Vrije Universiteit of Amsterdam.

The repository contains three datasets. Each one is used to answer a different main question of the research. It is based on the <a href="https://github.com/BuzzFeedNews/2016-10-facebook-fact-check">"Fact-Checking Facebook Politics Pages"</a> dataset made by Buzzfeed. We edited this data for our own research purposes.

<h1>Data moderation</h1>
In the beginning, the dataset was sorted in a way that the analysts at Buzzfeed can take advantage of it. Unfortunately, the form of the rows in the dataset was not satisfactory to answer our questions easily. We had to delete/add/change the rows of the dataset in the following steps and according to each question.<br /><br />
The first step was to delete the unnecessary columns like, “Account_id”, “Post_id” and “date published”. All the previous columns are for indexing proposing and have no effect on how the questions are going to be answered.
Since we are concerned about the fact check rates in general, we replaced the given rate in the dataset as the following to make it easier to be counted and to analyse it. We would then have a scale of trueness from 3 to 0 instead of text strings that says something about the verdict of a certain post.<br /><br />
Posts which were rated mostly true were assigned with the number 3.<br />
Posts which were rated mixture of true and false were assigned with the number 2.<br />
Posts which were rated mostly false were assigned with the number 1.<br />
Posts which were rated with no factual content were assigned with the number 0.<br /><br />
We added a column to sum up the interaction statistic numbers. We considered “Share_count”, “reaction_count” and “comment_count” as “Total_counts”. Any interaction on any post no matter how it was, eventually is an interaction.<br /><br />
We filled in the missing empty information from the cells, like in “debate” column, where the only filled in cells were the “yes” cells. In the “reaction_count”, “comment_count” and “Total_counts” as well there were some empty cells which were filled up with a “0”.<br /><br />

The above mentioned steps were needed to prepare the dataset properly in order to answer our question. Then, we had to conduct specific steps for each answer as follows:<br /><br />

For the first subquestion:
Does the interaction rate of false posts differ from true posts on Facebook? <br />
we made 4 extra sheets for each category: “Mostly True”, “mixture of true and false”, “mostly false” and “no factual content”. We filtered the dataset according to these categories and summed up the count of total posts in each category. The unnecessary columns like “Category”, “Page”, “Post URL”, “Debate” and “Post type” were removed. To get an answer to the question how many the posts in each different category were shared online, we divided the total amount of shares, reactions and comments with the total amount of posts in each different rating category. The resulting table can be found in the results of the project report.<br /><br />

For the second subquestion: Are the topics of false posts more often subject of debates than topics of true posts?<br />
we added 2 extra sheets for each debate option: Debate_yes and Debate_No. The only columns that we left are: “Rating”, “Debate” and “Total counts”. In order to know how many a post of each different rating category led to a debate, we let Excel count the amount of posts in the different rating categories that were in the Debate_yes and Debate_No sheets. The resulting table can be found in the results of the project report.
<br /><br />
For the third question: Which organizations post the most false information and which ones post the most true information?<br />
we created an extra sheet for each organization. The unnecessary columns were removed, like “Category”, “Post URL”, “Post type”, “Debate”, “Share_count”, “reaction_count”, “Comment_count” and “Total counts”. In order to answer the question, we let Excel count the amount of posts with the different ratings in each organisation sheet. To compare the number of posts between the organisations, we calculated the relative amount of posts in each rating category. We divided for example the amount of true posts with the total amount of posts in that organisation. The resulting table can be found in the results of the project report.
