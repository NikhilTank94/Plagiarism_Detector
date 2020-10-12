# Plagiarism-Detection-using-Pytorch
In this project, you will be tasked with building a plagiarism detector that examines a text file and performs binary classification; labeling that file as either plagiarized or not, depending on how similar that text file is to a provided source text. Detecting plagiarism is an active area of research; the task is non-trivial and the differences between paraphrased answers and original work are often not so obvious.

## Containment
One of your first tasks will be to create containment features that first look at a whole body of text (and count up the occurrences of words in several text files) and then compare a submitted and source text, relative to the traits of the whole body of text.

## Calculating containment
You can calculate n-gram counts using count vectorization, and then follow the formula for containment: If the two texts have no n-grams in common, the containment will be 0, but if all their n-grams intersect then the containment will be 1. Intuitively, you can see how having longer n-gram's in common, might be an indication of cut-and-paste plagiarism.

## Steps
**Notebook 1: Data Exploration**
•	Load in the corpus of plagiarism text data.
•	Explore the existing data features and the data distribution.
•	This first notebook is not required in your final project submission.

**Notebook 2: Feature Engineering**
•	Clean and pre-process the text data.
•	Define features for comparing the similarity of an answer text and a source text, and extract similarity features.
•	Select "good" features, by analyzing the correlations between different features.
•	Create train/test .csv files that hold the relevant features and class labels for train/test data points.

**Notebook 3: Train and Deploy Your Model in SageMaker**
•	Upload your train/test feature data to S3.
•	Define a binary classification model and a training script.
•	Train your model and deploy it using SageMaker.
•	Evaluate your deployed classifier.
