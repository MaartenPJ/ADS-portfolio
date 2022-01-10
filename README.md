# ADS-portfolio Maarten de Jonge 
## Student number 17113571

# DataCamp Course
From the DataCamp Courses, I completed the following:
-
-
-

Screenshots of the statements of accomplishment can be found here [#insert link]

# Reflection and Evaluation
- own contribution
situations:
  paper
several chapters in the paper
several presentations
research feature engineering audio files
binary models
several linear and convolutional NN's (eventually unused)
Meetings and (good) ideas
Research
Data exploration
Data preparation
Data visualisation
big picture planning of the minor
solving bugs or other issues whenever asked
Vast nog wel iets


Early on in the minor, my task was researching which machine learning algorithms could be used on audio recognition, how to use them and what was common practice in the field of data science. For most machine learning (not deep learning) algoritms it is nescessary to identify and engineer features for the model to use in training. 
After reading several articles, papers, websites, etc. I found no information on extracting features from eating sounds. Most instead opted for deep learning. 
After this, I made some visualisations of the data (waveform and spectrogram) and could not distinguish any clear commonalities between different positive samples.
I then decided that we should first try a neural network.
When I talked to the other groups using audio (emotions and dialogue), I heard that they were able to use spectrograms and MFCC's to create identifying features for different people/emotions. In one of the weekly meetings, one of the teachers also said MFCC's might help solve this problem.
After hearing this, I decided to try the same, but this did not lead to any usable data. It seemed that eating sounds were too differrent from speech to use the same methods.
After I relayed this to my group, we decided to focus on deep learning over machine learning, to circumvent the need for feature extraction by humans.

At several occasions while working together, a group member complained about a bug in their code or some other problem. Most of these times, I was able to fix or lessen the problem quickly.

I wrote a significant part of the final paper and I presented (parts of) 5 presentations. 2 external and 3 internal presentations. 
A more detailed description of my contribution to the paper can be found in Communication - writing paper.

Alongside the multiclass classifier models, I used the same dataset (with the same train-test split) and similar techniques to create binary classifier models. There were three reasons for doing this. 
Firstly we noticed a significant percentage of samples in our validation and test sets was misclassified between eating and drinking. I reasoned training a model on only eating or drinking sounds, not both, was a possible way to improve the results of our project.
Secondly it may happen (especially during an actual meal) that eating and drinking sounds occur in the same sample. If you want to keep track of both eating and drinking, detecting them with separate models will work better in such a case. Also there is no telling what result a multiclass classifier would give then.
The third reason was scientific curiosity.
I made binary classifier models to distinguish eating vs not eating, drinking vs not drinking and eating and drinking vs neither. [insert links to notebooks]
The binary models to distinguish only eating were comparable to the multiclass classifiers in terms of accuracy and comparable or sometimes slightly better in terms of precision. The binary models for only drinking performed consistently slightly worse than both the multiclass classifiers and the other binary models. The binary model to distinguish eating or drinking vs neither performed only slightly worse than the only eating binary classifier.
[This was a clear indication that eating sounds differ enough from drinking sounds to alter the performance of a model.]

- learning objectives
Data science skills/knowledge
Working in a team
Using Scrum properly



- group project as a whole

# Research Project
- task definition
Our group was one of three to work for the Smart Teddy Project under supervision of Hani Al-Ers. This project aims to help in the care of elders with beginning cases of dementia by introducing a teddy bear in their home that uses sensors to monitor their quality of life.
Our group, "Team Nourish", was tasked with finding an algorithm that can distinguish eating (and less importantly drinking) sounds from ambient/background/other sounds around the house.
Our chosen research question was "Which deep learning model is optimal to detect eating and drinking sounds from audio?"
Furthermore, after talking with the problem owner, we decided to define "optimal" as a high accuracy score, but with a secondary emphasis on precision. This is because the problem owner would rather have the teddy bear miss a meal and have a caretaker check up an additional time (False Negative), than the teddy reporting meals that didn't happen, potentially resulting in a malnourished senior.
The reason accuracy was chosen as the leading metric despite the wish for high precision, was that focussing on accuracy during training resulted in a better overall model.

- evaluation
In future studies about this problem, I would advise more research into applying binary classifiers. Our group decided to focus on multiclass classifiers after initial experimentation in both binary and multiclass classifiers. This would have the teddy need only a single model instead of two. 
Later in the project, however, we decided to revisit the binary classifier idea. The resulting models were quite promising and certain binary classifiers even outperformed their multiclass classifier equivalents in certain specific metrics.
[We unfortunately didn't have enough time to spend on this avenue until the very end of the project, due to the fact that we only had half of our initial group for most of the project.]
I recommend taking several different splits between training/validation/test sets to see if the results are not caused by unrepresentative data in the test set.
[insert more recommendations here]

- conclusions
[more here]
Unfortunately our best individual result was with a ResNet transfer learning model, but due to the incredible fluctuations between epochs on all these models, we could not confidently recommend any of these models as the optimal model. We concluded, that the ResNet models we trained were too unreliable.
[more here]

- planning
Our group has used Scrum in the planning of this project. We made a Scrum board on Jira and ended up with over a hundred total tickets.
At several moments during the minor, I sensed a lull was coming up due to some group members not knowing their tasks. In several of these moments, I called for an extra meeting to discuss our plans for the rest of the minor.
Our planning being agile due to scrum caused the group to deviate from these plans several times, but the overview of current tasks was appreciated by all group members.

[insert link to scrum board]


# Predictive analytics
- selecting model
- configuring model
- training model
- evaluating model
- visualising outcome model

# Domain Knowledge
- intro subject field
- literature research
[link to file containing many links about data science and stuff]

- explanation of terminology, jargon, definitions
[Collect a list of words and explain them I guess]
Machine Learning
Deep Learning
Back propagation
Features
feature engineering
epoch
(validation) loss
accuracy
precision
recall
confusion matrix
model
dropout
activation function
linear layer
convolution
Neural Network
overfitting
underfitting
regression
forest
crossentropy



# Data Preprocessing
- data exploration
[Find and reference all python files/notebooks used for data visualisation]
[describe how you explored the data]
[describe early hypotheses]
In the beginning, the research question was a different one, namely "Is it possible to detect eating and drinking sounds from audio using machine/deep learning?" Early Data exploration of the new/final dataset revealed very clear patterns in several of the eating and drinking sounds (recognisable and comparable bands in spectrograms)[insert references to a spectrogram with these bands]. This strengthened our confidence, that our assignment was indeed possible.

- data cleansing
The data was not cleaned, because we were not certain what we were looking for, so passing it through for example a low-pass noise reduction filter could remove the relevant identifiers the models should be looking for.
Furthermore, the Google Audioset contained mostly samples that had very little static/noise, so reducing this was not nescessary.
Later, during data enhancement, more background noises were even added to make the samples more like a realistic recording from the teddy bear.

- data preparation
After the initial exploration of the dataset, we noticed the positive samples for both eating and drinking made up only a small percentage of the dataset. We decided to enlarge the amount of samples using data augmentation. To ensure the models would train on the data, not the augmentations, the same enhancements were performed on the negative samples.
This work was largely done by Florian, with me providing help where asked.


- data explanation
The dataset consists of audio files taken from Google databases (mostly YouTube). Since most of these files were at a length of approximately 10 seconds, all files were made to be exactly 10 seconds long.
The name of the dataset used is Google AudioSet. [insert link to audioset] It contains millions of snippets of audio labeled with a description of their contents. These labels include things like vacuuming, breathing, [insert labels here], but most relevantly chewing and drinking. 


- data visualisation

# Communication
- presentations
I presented 3 internal presentations, of which 1 alone and 2 with another member of the group.
I also presented 2 external presentations, of which 1 alone and 1 with another group member.

- paper
I, together with lucas, laid down the structure for the paper.
In the paper I contributed in large part to the chapters ............
I also helped the other members of my team with questions about scientific writing and 