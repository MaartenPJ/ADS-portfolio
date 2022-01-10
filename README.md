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
several chapters in the paper\
several presentations\
research feature engineering audio files\
binary models\
several linear and convolutional NN's (eventually unused)\
Meetings and (good) ideas\
Research\
Data exploration\
Data preparationX
Data visualisation\
big picture planning of the minor\
solving bugs or other issues whenever asked\
Vast nog wel iets [ja wat dan]


Early on in the minor, my task was researching which machine learning algorithms could be used on audio recognition, how to use them and what was common practice in the field of data science. For most machine learning (not deep learning) algoritms it is nescessary to identify and engineer features for the model to use in training. 
After reading several articles, papers, websites, etc. I found no information on extracting features from eating sounds. Most instead opted for deep learning. 
After this, I made some visualisations of the data (waveform and spectrogram) and could not distinguish any clear commonalities between different positive samples.
I then decided that we should first try a neural network.
When I talked to the other groups using audio (emotions and dialogue), I heard that they were able to use spectrograms and MFCC's to create identifying features for different people/emotions. In one of the weekly meetings, one of the teachers also said MFCC's might help solve this problem.
After hearing this, I decided to try the same, but this did not lead to any usable data. It seemed that eating sounds were too differrent from speech to use the same methods.
After I relayed this to my group, we decided to focus on deep learning over machine learning, to circumvent the need for feature extraction by humans.


Alongside the multiclass classifier models, I used the same dataset (with the same train-test split) and similar techniques to create binary classifier models. There were three reasons for doing this. 
Firstly we noticed a significant percentage of samples in our validation and test sets was misclassified between eating and drinking. I reasoned training a model on only eating or drinking sounds, not both, was a possible way to eliminate (some of) these errors and improve the results of our project.
Secondly it may happen that eating and drinking sounds occur in the same sample. If you want to keep track of both eating and drinking separately, detecting them with separate models will work better. Also there is no telling what result a multiclass classifier would give for such a sample.
The third reason was scientific curiosity.
I made binary classifier models to distinguish eating vs not eating, drinking vs not drinking and eating and drinking vs neither. [insert links to notebooks]
To keep consistency between the binary and multiclass models, I used almost the same code as Florian to load in and label the data, replacing certain variables as nescessary.
The binary models to distinguish only eating were comparable to the multiclass classifiers in terms of accuracy and comparable or sometimes slightly better in terms of precision. The binary models for only drinking performed consistently slightly worse than both the multiclass classifiers and the other binary models. The binary model to distinguish eating or drinking vs neither performed only slightly worse than the only eating binary classifier.
The fact that recognising drinking performed the worst out of the binary models corresponds to the results of the multiclass classifiers, which also usually performed better on eating than drinking. This implies that, at least for our dataset, drinking sounds are inherently more difficult to classify than eating sounds.
Because the results for eating were on average comparable to the multiclass classifiers, the results for drinking were consistently worse and there had already been a lot of work put in to the multiclass models, we decided not to pursue the binary models any further as a final product.


I experimented with several different models (mainly neural networks). The goal of these experiments was mostly to further my own understanding of how to make a model.
[These models scored slightly lower than another model that one of my group members made around the same time, so it was decided not to continue working on this version.]


At several occasions while working together, a group member complained about a bug in their code or some other problem. Most of these times, I was able to help fix or lessen the problem quickly.
I played a part in the meetings the group had. These include internal meetings, meetings with teachers, meetings with the problem owner and meetings with other project groups.
I took the lead at several times to ensure a good planning and equal division of tasks for all members of the group.

I did research into several data science-related topics. A list of articles I read can be found here [insert link] [Existing research on audio recognition and eating sounds in particular, general information on making/training/learning models]

Data exploration consisted of several different actions: looking at the amount of samples, the distribution of labels among samples, listening to the individual audio fragments, creating waveforms and spectrograms of them, studying those images for patterns and/or irregularities, verifying that the samples were correctly labeled, etc. I performed several of these actions for each of the considered datasets. (Over all datasets combined, I performed all of these actions)

I wrote some scripts to visualise audio in several different forms (waveform, fft, (regular) spectrogram, mel spectrogram, MFCC) [link to scripts]

I wrote a significant part of the final paper and I presented (parts of) 5 presentations. 2 external and 3 internal presentations. 
A more detailed description of my contribution to the paper can be found further on in this document in the part Communication - writing paper.

- learning objectives
Learning Objective: Acquire data science skills/knowledge
Situation:
I was interested in data science, but had little knowledge and skills on the subject.
Task:
Expand my knowledge on the subject and improve my skills.
Action:
Read many articles online, researching the best methods to tackle the problems I encountered. Attend lectures about the subjects. Speak with teachers and peers. Practice relevant programming exercises (e.g. DataCamp, notebooks). Work on the assignment give to me by the problem owner (identifying eating and drinking sounds from audio using machine/deep learning)
Result:
After reading articles, looking at examples of how other research groups attempted to solve similar problems, I learned not only how to program a neural network that can recognise specific sounds, but also how to structure such a project and after attempting several things myself and with other members of my group, I also learned what things to try and where to put priorities.
Reflection:
I think if I were to start another similar project, I would have a much easier time, due to the skills I have acquired in the last few months.
I am satisfied with the amount I have learned. I have contributed at least in part on every aspect of the final product and understand not only which choices were made, but also why they were made.
However, over the course of the minor I have been hindered several times by health-related issues. If this hadn't been the case, I would have liked to play and experiment with the subject matter more, instead of only doing what was required of me.


Learning Objective: Improving (Python) programming skills
Situation:
I had already finished several physics-related courses in my major, which required some programming in Python. I wished to improve and polish my skills by doing a minor that was more computer science-related.
Task:
Practicing with Python and learning new features and conventions.
Action:
Programming several Python scripts over the course of the 18-week minor and following the courses on DataCamp
Result:
I learned many things Python can be used for, which I hadn't encountered before, even in modules I had used in previous situations like matplotlib and pandas.
I also became faster at planning and coding programs by practicing.
Reflection:
I am happy to see, that, even though I had not done too much programming in the past few years, I quickly got into the programming mindset. I programmed several different types of scripts/programs and was able to learn new skills rather quickly. This also allowed me to help the other members in my team with troubleshooting errors and bugs (even the computer science students).
I will certainly have use of my acquired skills in further study and my later job.


Learning Objective: Working in a team
Situation:
This minor required me to work in an international, multidisciplinary team to work on the project. I have worked in several different teams in the past with varying levels of efficiency and cooperation.
Task:
From the start of the minor, I was determined to try to take an active role in ensuring the tasks were planned ahead properly and the work was divided equally among the members of the group.
Action:
From the beginning, I insisted on meeting physically multiple times per week to discuss progress and planning and to ensure everyone was up to date on decisions being made. I also at certain points initiated an extra meeting if I noticed or suspected that the group was not functioning properly.
I also made a point of communicating changes that would affect the work of other members immediately.
Result:
The team finished every task in time and almost every major decision was first discussed and weighed. I played my part in this project team and contributed not only my own knowledge on the subject matter, but also my communications skills, which I acquired elsewhere.
Reflection:
I experienced the teamwork as pleasant during almost every part of the minor. I took an active role in the discussions whenever I thought my input would be relevant, but also tried not to come off as too dominant a person.
I think I can use the experiences from this team to my benefit in any future teams I will be a part of.


- group project as a whole
At the start 3 people didnt show up, then 2 of those did, then 1 left, then another left.
Only half the intended group size.
Teachers advised us to prioritise due to this and not try to explore every possible avenue.
First few weeks lot of individual working without much collaborating or vision of the goal.

After several weeks, the group started meeting and discussing more in-depth and efficiently. 
We communicated more about new discoveries and insights and changes in plans. This lead to a pleasant working environment.
The communication was very open throughout the minor.
Even though all group members came from different countries, there were little to no language-related barriers in communication.

I am satisfied with the results of the project. The final model is not perfect, but likely good enough for the purposes of the problem owner. Also I believe it is the best we could have done considering the assignment and the fact there were only 3 people for most of the project.

[talk more about my role in all this maybe?]

Situation:
As a part of his Smart Teddy project, 
Task:



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
In the beginning, the research question was a different one, namely "Is it possible to detect eating and drinking sounds from audio using machine/deep learning?" Early Data exploration of the new/final dataset revealed very clear patterns in several of the eating and drinking sounds (recognisable and comparable bands in spectrograms)[insert references to a spectrogram with these bands]. This strengthened our confidence, that our assignment [recognising these sounds] was indeed possible.

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
