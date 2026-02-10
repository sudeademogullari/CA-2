CA 2
Project Goal
In this project, a Naive Bayes model is trained to be used to determine spam or not spam
emails. Spam emails are marked 1 and Non spam emails are marked 0. The model predicts
using the words contained in the emails.

Data
Two folders which are used by the project are the ones named train-mails and test-mails. The
former is applied to train the model and the latter is applied to test the model. When there is a
file name beginning with spmsg, the mail is marked as spam. Otherwise, it will be considered as
non-spam.

Method
The initial step of the program is to create a dictionary of 3000 most frequent words in the
training mail. Then every email is converted to a row of numbers which indicates the number of
times a word is repeated. The program leaves out the first two lines of every email and begins
with the third line. Then, a Gaussian Naive Bayes model is trained using training data then
tested using the test data. It is also given an accuracy score which is printed at the end.

Step 1: Build a Dictionary
Read all training emails
Collect all words
Remove:
Numbers and symbols
One-letter words
Keep the 3000 most common words
These words become our features

Step 2: Convert Emails to Numbers (Features)
Each email becomes a row of numbers
Each column = one word from the dictionary
The value = how many times that word appears in the email
We skip the first 2 lines of each email and start from line 3
We also create a label for each email:
Spam = 1
Not Spam = 0

Step 3: Train and Test the Model
Build dictionary from training data
Convert training emails to numbers
Convert test emails to numbers
Train the Gaussian Naive Bayes model
Predict labels for test emails
Calculate and print accuracy

Output
The program prints the accuracy of the model on the test data.

How to Run
Ensure that train-mails and test-mails folders are at the same location with the notebook.
