## Challenge 3: Natural Language Processing

### Overview

Sentiment analysis is a rapidly growing field, as large databases become increasingly available, and companies have an interest in automatically extracting sentiment from internet users.

With the increasing amount of content and debate on social media platforms such as Twitter, there is an interest in automatically extracting meaning and sentiment from users' posts, to be able to evaluate the aggregate opinion of a large number of users. Capturing sentiment in language is important in these times where decisions and reactions are created and updated in seconds.

For this challenge, students are provided with tweets from [Figure Eight's Data for Everyone platform](https://en.wikipedia.org/wiki/Figure_Eight_Inc.). Your task will be to classify tweets with positive, neutral, or negative labels, reflecting the sentiment of the user writing the tweet.

For example:

- "I love this ice-cream, it is so good ! :-)" -> positive.
- "Last week I visited San Francisco" -> neutral.
- "Disappointed by the last Avengers movie..." -> negative.

The performance criterion is based on your model's ability to predict the correct labels for the testing data.

At the end of the challenge, if you wish to do so, there is a bonus task which consists of detecting the relevant words inside the tweet which are most responsible for the attributed sentiment. For example in the phrase "I really like this song", the relevant words are: "really like".

### Dataset Description

- train.csv - the training set
- test.csv - the test set
- sample_submission.csv - a sample submission file in the correct format, containing random predictions

The sample_submission.csv file is currently not used: it is a sample submission file in the correct format, that is used in automatic evaluation platforms such as Kaggle. You can discard this file.

### How to access the data?

The dataset we use is a selection of the original one used in the official competition. You can download the data (and have a look at it) from my [Kaggle dataset page](https://www.kaggle.com/datasets/michiard/sentiment-analysis-dataset).

Here you have two choices: either you download the data and use it on your laptop or upload it back to for example your Google drive for accessing it using a Google Notebook, or you can use the Kaggle platform. In this last case, you can either clone the dataset, or try to access it directly from my dataset page, through your Kaggle Kernel (called notebook).

### Metrics

The evaluation metric for this competition is [Macro F1-Score](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.fbeta_score.html#sklearn.metrics.fbeta_score). The F1 score, commonly used in information retrieval, measures accuracy using the statistics precision p and recall r. Precision is the ratio of true positives (tp) to all predicted positives (tp + fp). Recall is the ratio of true positives to all actual positives (tp + fn). The Macro F1-Score takes the mean score over all classes.

**Bonus:** For the bonus task, your can estimate the overlap between your prediction, and the selected words ground truth using the [Jaccard coefficient](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.fbeta_score.html#sklearn.metrics.fbeta_score), which measures the ratio of intersection to union of predicted and label sets.

### Important note:

Where are my labels? You will notice that the test set (clearly) has no labels! This is used in a "real world" challenge, whereby you are asked to predict labels for unseen data during training. Labels are "kept secret" by the challenge organizers, and the automatic evaluation system uses a submission file to compare to the "secret ground truth".

Since we will not have this step in the AML course, you are tasked with the important goal of splitting your training set, and hold out validation and test data to check the performance of your model.
