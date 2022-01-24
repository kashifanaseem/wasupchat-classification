# wasupchat-classification
text classification on a raw chat data from scratch

**Introduction:** Data was given in a text file and taken from a whatsapp chat, with 
two column given, Date and Text. Aim was to find insights from the data.

**Methodology:** For this few steps were considered given below:
 First difficulty was part of messages were in Date column because of text 
file, it was handled by changing date in datetime format to separate string 
from date column and to add in previous text to create a full text.
 Second, data included some info messages like group created, someone 
left, somebody has been added etc. These messages do not include any 
important information so that was tackled by labeling it as Info and rest as 
Msg.
 Third, Messages were not labelled as these are some query or some 
answers to queries or any kind of neutral message, for that collected a 
small data from the given data of 40 rows, included neutral, query, answers 
and labelled it manually. Then used this small data to build a temporary 
model to tag the actual data. For training, required a training and test data, 
divided the data in to 80-20% for train-test data. Trained the model on 80% 
data and got 90% accuracy on 20% test data. Then checked wrongly 
predicted data, if it’s wrongly tagged by first model it can be corrected and 
need to re train actual model to increase the accuracy.
 Fourth, for more included a word cloud to check words used mostly in chat, 
selected few words with higher occurrence. Can also add topic model 
further
