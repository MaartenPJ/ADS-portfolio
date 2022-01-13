# ADS-portfolio Maarten de Jonge 
## Student number 17113571

[1. DataCamp](https://github.com/MaartenPJ/ADS-portfolio#1-datacamp-course)
[2. Reflection and evaluation](https://github.com/MaartenPJ/ADS-portfolio#2-reflection-and-evaluation)
[3. Research Project](https://github.com/MaartenPJ/ADS-portfolio#3-research-project)
[4. Predictive Analytics](https://github.com/MaartenPJ/ADS-portfolio#4-predictive-analytics)
[5. Domain knowledge (not done)](https://github.com/MaartenPJ/ADS-portfolio#5-domain-knowledge)
[6. Data preprocessing](https://github.com/MaartenPJ/ADS-portfolio#6-data-preprocessing)
[7. Communication](https://github.com/MaartenPJ/ADS-portfolio#7-communication)


# 1 DataCamp Course
From the DataCamp Courses, I completed the following:
- Introduction to Python
- Intermediate Python
- Python Data Science Toolbox (Part 1)
- Python Data Science Toolbox (Part 2)
- Statistical Thinking in Python
- Supervised Learning with scikit-learn
- Introduction to Data Visualisation with Matplotlib
- Machine Learning for Time Series Data in Python
These are 8/16 courses or 50%

Screenshots of the statements of accomplishment can be found [here](https://github.com/MaartenPJ/ADS-portfolio/tree/main/DataCamp).

I decided not to do every course. Some covered topics I had already studied before the minor and some covered topics, that I had already researched and done myself for this minor. I did look at all the video's to make sure there was no important information, that I would miss.

[Back to top](https://github.com/MaartenPJ/ADS-portfolio#ads-portfolio-maarten-de-jonge)

# 2 Reflection and Evaluation
## 2.1 Reflection on own contribution to the project
Exploring machine learning for classifying audio data:\
Situation:\
A model needed to be chosen.

Task:\
Early on in the minor, my task was researching which machine learning algorithms could be used on audio recognition, how to use them and what was common practice in the field of data science. 

Action:\
For most machine learning (not deep learning) algoritms it is nescessary to identify and engineer features for the model to use in training.\
After reading several articles, papers and websites(see [literature list](https://github.com/MaartenPJ/ADS-portfolio/blob/main/Literature%20List%20Portfolio.docx)), I found no information on extracting features from eating sounds. Most instead opted for deep learning. \
After this, I made some visualisations of the data (waveform and spectrogram) and could not distinguish any clear commonalities between different positive samples.\
I then decided that we should first try a neural network.\
I talked to the other groups using audio (emotions and dialogue). I heard that they were able to use spectrograms and MFCC's to create identifying features for different people/emotions. In one of the weekly meetings, one of the teachers also said MFCC's might help solve this problem.\
After hearing this, I decided to try the same, but this did not lead to any more usable data. 

Result:\
It seemed that eating sounds were too different from speech to use the same methods.\
After I relayed this to my group, we decided to focus on deep learning over machine learning, to circumvent the need for feature extraction by humans.

Reflection:\
I think using deep learning was the right choice. After seeing the final results of other groups, they also moved to deep learning later in the project, because it gave better results.\
I think that recognising early on, that feature engineering is difficult for eating sounds, has saved the group a lot of work, that might have been for nothing.



Binary classifiers:\
Situation:\
There were three reasons for making binary classifiers.\
Firstly we noticed a significant percentage of samples in our validation and test sets was misclassified between eating and drinking. I reasoned training a model on only eating or drinking sounds, not both, was a possible way to eliminate (some of) these errors and improve the results of our project.\
Secondly it may happen that eating and drinking sounds occur in the same sample. If you want to keep track of both eating and drinking separately, detecting them with separate models will work better. Also there is no telling what result a multiclass classifier would give for such a sample.\
The third reason was scientific curiosity.

Task:\
Make binary classifiers, that are similar to the existing multiclass classifiers. Compare the results of both.

Action:\
Alongside the multiclass classifier models, I used the same dataset (with the same train-test split) and similar techniques to create binary classifier models.\
I made binary classifier models to distinguish eating vs not eating, drinking vs not drinking and eating and drinking vs neither.\
To keep consistency between the binary and multiclass models, I used almost the same code as Florian to load in and label the data, replacing certain variables as nescessary.\
The notebooks used are found [here](https://github.com/MaartenPJ/ADS-portfolio/blob/main/Binary%20model%20notebooks/Binary%20Models%20Drink-no.ipynb), [here](https://github.com/MaartenPJ/ADS-portfolio/blob/main/Binary%20model%20notebooks/Binary%20Models%20Eat-no.ipynb) and [here](https://github.com/MaartenPJ/ADS-portfolio/blob/main/Binary%20model%20notebooks/Binary%20Models%20EatDrink-no.ipynb)

Results:\
The binary models to distinguish only eating were comparable to the multiclass classifiers in terms of accuracy and comparable or sometimes slightly better in terms of precision. The binary models for only drinking performed consistently slightly worse than both the multiclass classifiers and the other binary models. The binary model to distinguish eating or drinking vs neither performed only slightly worse than the only eating binary classifier.\
The fact that recognising drinking performed the worst out of the binary models corresponds to the results of the multiclass classifiers, which also usually performed better on eating than drinking. This implies that, at least for our dataset, drinking sounds are inherently more difficult to classify than eating sounds.\
We decided not to pursue the binary models any further as a final product, because the results for eating were on average comparable to the multiclass classifiers, the results for drinking were consistently worse and there had already been a lot of work put in to the multiclass models.

Reflection:\
I think I explored the option of using binary models extensively. I am happy, that I was able to make the results of these models almost as good as the multiclass classifiers. I personally wish, we continued working on the binary classifiers more, but I understand the decision of the group and agree, that this was the best course of action at the time.

Other contributions:\
I experimented with several different models (mainly neural networks). The goal of these experiments was mostly to further my own understanding of how to make a model, not nescessarily to further project itself.

At several occasions while working together, a group member complained about a bug in their code or some other problem. Most of these times, I was able to help fix or lessen the problem quickly.\
I played a part in the meetings the group had. These include internal meetings, meetings with teachers, meetings with the problem owner and meetings with other project groups.\
I took the lead at several times to ensure a good planning and equal division of tasks for all members of the group.

I did research into several data science-related topics. A list of articles I read can be found [here](https://github.com/MaartenPJ/ADS-portfolio/blob/main/Literature%20List%20Portfolio.docx). This list is, unfortunately, not comprehensive. \

I performed data exploration. Data exploration consisted of several different actions: looking at the amount of samples, the distribution of labels among samples, listening to the individual audio fragments, creating waveforms and spectrograms of them, studying those images for patterns and/or irregularities, verifying that the samples were correctly labeled, etc. I performed several of these actions for each of the considered datasets. Over all datasets combined, I performed all of these actions.

I wrote some scripts to visualise audio in several different forms (waveform, fft, (regular) spectrogram, mel spectrogram, MFCC) [link to scripts](https://github.com/MaartenPJ/ADS-portfolio/blob/main/notebooks/Data%20Visualisation.ipynb)

I wrote a significant part of the final paper and I presented (parts of) 5 presentations. 2 external and 3 internal presentations. I also took part in creating most powerpoints, as we usually created those in a meeting with the whole group.\
I got compliments on my fluency and from feedback during meetings, I think I got the information across in a comprehensible way.\
A more detailed description of my contribution to the paper can be found further on in this document in part [7.2 Writing paper](https://github.com/MaartenPJ/ADS-portfolio#72-writing-paper).

## 2.2 Reflection on own learning objectives
Learning Objective: Acquire data science skills/knowledge\
Situation:\
I was interested in data science, but had little knowledge and skills on the subject.

Task:\
Expand my knowledge on the subject and improve my skills.

Action:\
Read many articles online, researching the best methods to tackle the problems I encountered. Attend lectures about the subjects. Speak with teachers and peers. Practice relevant programming exercises (e.g. DataCamp, notebooks). Work on the assignment given to me by the problem owner (identifying eating and drinking sounds from audio using machine/deep learning)

Result:\
After reading articles, looking at examples of how other research groups attempted to solve similar problems, I learned not only how to program a neural network that can recognise specific sounds, but also how to structure such a project and after attempting several things myself and with other members of my group, I also learned what things to try and where to put priorities.

Reflection:\
I think if I were to start another similar project, I would have a much easier time, due to the skills I have acquired in the last few months.\
I am satisfied with the amount I have learned. I have contributed at least in part on every aspect of the final product and understand not only which choices were made, but also why they were made.\
However, over the course of the minor I have been hindered several times by health-related issues. If this hadn't been the case, I would have liked to play and experiment with the subject matter more, instead of only doing what was required of me.

Learning Objective: Improving (Python) programming skills\
Situation:\
I had already finished several physics-related courses in my major, which required some programming in Python. I wished to improve and polish my skills by doing a minor that was more computer science-related.

Task:\
Practicing with Python and learning new features and conventions.

Action:
Programming several Python scripts over the course of the 18-week minor and following the courses on DataCamp.

Result:\
I learned many things Python can be used for, which I hadn't encountered before, even in modules I had used in previous situations like matplotlib and pandas.\
I also became faster at planning and coding programs by practicing.

Reflection:\
I am happy to see, that, even though I had not done too much programming in the past few years, I quickly got into the programming mindset. I programmed several different types of scripts/programs and was able to learn new skills rather quickly. This also allowed me to help the other members in my team with troubleshooting errors and bugs (even the computer science students).\
I will certainly have use of my acquired skills in further study and my later job.


## 2.3 Evaluation on the group project as a whole
In the first 8 weeks of the minor, the amount of people in the group changed 3 times.\
Afterwards, we were left with only half the intended group size.\
Teachers advised us to prioritise due to this and not try to explore every possible avenue.\
The first few weeks consisted of a lot of individual working without much collaborating or vision of the goal.

After several weeks, the group started meeting and discussing more in-depth and efficiently.\
We communicated more about new discoveries and insights and changes in plans. This lead to a pleasant working environment.\
The communication was very open throughout the minor.\
Even though all group members came from different countries, there were little to no language-related barriers in communication.

I am satisfied with the results of the project. The final model is not perfect, but likely good enough for the purposes of the problem owner. Also I believe it is the best we could have done considering the assignment and the fact there were only 3 people for most of the project.

Situation:\
This minor required me to work in an international, multidisciplinary team to finish a project. I have worked in several different teams in the past with varying levels of efficiency and cooperation.

Task:\
From the start of the minor, I was determined to try to take an active role in ensuring the tasks were planned ahead properly and the work was divided equally among the members of the group.

Action:\
From the beginning, I insisted on meeting physically multiple times per week to discuss progress and planning and to ensure everyone was up to date on decisions being made. I also at certain points initiated an extra meeting if I noticed or suspected that the group was not functioning properly.\
I also made a point of communicating changes that would affect the work of other members immediately.

Result:\
The team finished every task in time and almost every major decision was first discussed and weighed. I played my part in this project team and contributed not only my own knowledge on the subject matter, but also my communications skills, which I acquired elsewhere.

Reflection:\
I experienced the teamwork as pleasant during almost every part of the minor. I took an active role in the discussions whenever I thought my input would be relevant, but also tried not to come off as too dominant a person.\
I think I can use the experiences from this team to my benefit in any future teams I will be a part of.

[Back to top](https://github.com/MaartenPJ/ADS-portfolio#ads-portfolio-maarten-de-jonge)

# 3 Research Project
[Our paper](https://github.com/MaartenPJ/ADS-portfolio/blob/main/Paper/ResearchPaperNourish.pdf)\
[Notebook containing our final model](https://github.com/MaartenPJ/ADS-portfolio/blob/main/notebooks/cnn2-tuning.ipynb)

## 3.1 Task definition
Our group was one of three to work for the Smart Teddy Project under supervision of Hani Al-Ers. This project aims to help in the care of elders with beginning cases of dementia by introducing a teddy bear in their home that uses sensors to monitor their quality of life.\
Our group, "Team Nourish", was tasked with finding an algorithm that can distinguish eating (and less importantly drinking) sounds from ambient/background/other sounds around the house.\
Our chosen research question was "Which deep learning model is optimal to detect eating and drinking sounds from audio?"\
Furthermore, after talking with the problem owner, we decided to define "optimal" as a high accuracy score, but with a secondary emphasis on precision. This is because the problem owner would rather have the teddy bear miss a meal and have a caretaker check up an additional time (False Negative), than the teddy reporting meals that didn't happen, potentially resulting in a malnourished senior.\
The reason accuracy was chosen as the main metric despite the problem owner's wish for high precision, was that focussing on accuracy during training resulted in a better overview of the models. We also checked if it negatively impacted the precision scores, but the difference in precision scores was negligible.

## 3.2 Evaluation
In future studies about this problem, I would advise more research into applying binary classifiers. Our group decided to focus on multiclass classifiers after initial experimentation in both binary and multiclass classifiers. This would have the teddy need only a single model instead of two.\
Later in the project, however, we decided to revisit the binary classifier idea. The resulting models were quite promising and certain binary classifiers even outperformed their multiclass classifier equivalents in certain specific metrics.

I recommend taking several different splits between training/validation/test sets to see if the results are not caused by unrepresentative data in the test set.

In hindsight, I would have liked to try varying the hyperparameters more. Especially with the ResNet models. These models all fluctuated greatly, which according to the lectures could be a sign of a value for learning rate which is too high. We optimised the learning rate for our own CNN's and used this value for the transfer learning models as well, which might not have been the optimal value for the different models.

I would recommend a new dataset also include eating-related sounds like cutlery on a plate, instead of only chewing and mastication sounds. This will provide additional signifying markers, that a CNN could recognise as eating.\
Additionally a dataset collected from the teddy bear itself would of course give a more representative result than a selection of Youtube-clips. Creating such a dataset would require a lot of manual labour in accurately labeling the samples, especially if the dataset is to be of significant size.

## 3.3 Conclusions
The research question was “Which deep learning model is optimal to detect eating and drinking sounds from audio?”\
The answer to the question is a convolutional neural network with 2 convolutional layers followed by 3 layers.

To reach this conclusion, there were several decisions to be made.\
First we had to decide whether to use a machine learning or deep learning algorithm. As I discussed in more detail in the first paragraph of [the "Own contribution" chapter](https://github.com/MaartenPJ/ADS-portfolio#21-reflection-on-own-contribution-to-the-project), we decided that deep learning would work better for this problem.\
After we decided on using neural networks, there were several, partly codependant, questions that needed to be answered next. These questions were, among others, how many layers, how many nodes per layer, whether to include convolution steps, what learning rate and batch size to use.\
Adding convolutional layers to the model turned out to improve performance regardless of the other hyperparameters, so deciding it should be a CNN was an easy choice. (The best performing strictly linear model had an accuracy of 66,4%. Almost all models with convolutional layers had an accuracy above 70%)\
The number of both convolutional and linear layers was varied and the result was that a CNN with 2 convolutional layers followed by 3 linear layers seemed to perform most optimally. This was the model with the best performance for both eating and drinking sounds.\
Later, we used transfer learning with ResNet models to try to make a better model. While these models produced scores in certain epochs, that exceeded our best "self-made" CNN's, looking at the accuracy and loss plotted against epochs made us believe this was a fluke. The best epoch, with an accuracy score of 83,6%, was followed immediately by an epoch with an accuracy score of 24,4%, for example. The relevant accuracy plot can be seen here [link] and as figure 6 in the paper.\
These huge inconsistencies led us to discount the ResNet models as candidates for an "optimal model".

## 3.4 Planning
Our group has used Scrum in the planning of this project. We made a Scrum board on Jira and ended up with 95 total tickets.\
We decided not to do the daily stand-up every day, but we did meet an average of 3 times per week to discuss progress.\
At several moments during the minor, I thought things were not going smoothly. In these cases, I called for an extra meeting to discuss our plans for the rest of the sprint/minor.\
Our planning being agile due to scrum caused the group to deviate from these plans several times, but the overview of current tasks was appreciated by all group members.\
Although the aim was to use Scrum for everything related to the project, sometimes an issue was discussed and then quickly resolved, without it ever reaching the Jira board.\
[Link to Scrum/Jira board](https://teamnourish.atlassian.net/jira/software/projects/NOUR/boards/1).

[Back to top](https://github.com/MaartenPJ/ADS-portfolio#ads-portfolio-maarten-de-jonge)

# 4 Predictive analytics
## 4.1 Selecting a model
The final model is a Convolutional Neural Network with 2 convolutional layers and 3 linear layers, aside from the input and output layers, of course. The choice for a CNN was made very early on in the minor, since our research online into how to perform audio classification resulted almost exclusively in articles recommending using a CNN to do this.\
Some of these articles are separated out at the bottom of [the literature list](https://github.com/MaartenPJ/ADS-portfolio/blob/main/Literature%20List%20Portfolio.docx).\
We did try neural networks without convolution as well, to verify a CNN was the best option, but these performed significantly worse on our data. This is clearly visible when comparing [the accuracy graph of the best linear NN](https://github.com/MaartenPJ/ADS-portfolio/blob/main/Images/Linear%20NN%20acc.png) to [the accuracy graph of the best CNN](https://github.com/MaartenPJ/ADS-portfolio/blob/main/Images/CNN%20acc.png).


## 4.2 Configuring a model
The exact shape of the CNN was decided experimentally.\
The amount of 2 convolutional layers was ideal, because the accuracy, precision and recall scores were better, than with 0 or 1 convolutional layers. More than 2 convolutional layers led to more overfitting.\
The same argument holds for 3 hidden linear layers. This was the highest amount of linear layers we could add, without noticing significant overfitting in the training curves.

## 4.3 Training a model
In training the first iterations of the model, we noticed the training and validation loss curves started diverging greatly after only a few epochs. This is a clear indication of overfitting. We theorised the most likely cause of this was that our model was too complex for the amount of data we had. To fix this, we tried several different things.\
We reduced the amount of nodes per linear layer from 1000 down to 100 (a number which stayed until the end of the project).\
We reduced the size of the samples fed to the models. We used a fixed-size mel spectrogram of 801 by 100 "pixels", instead of a full-resolution image. This increased the information density of our samples, reducing the chance of the model training on irrelevant patterns, like pixels that contain no data.\
We used data augmentation to increase the amount of samples. Later we found a new, larger dataset, which we also augmented, further increasing our total amount of samples.

Batch size 64 was chosen after trying several powers of 2, because it generated better scores than 32 and 16 and overfitted less than higher values.\
In our experiments, a learning rate of 0.001 was ideal for the CNN's. The training curves were quite smooth, but we are also pretty confident, that we reached the global optimum, because a greater learning rate never provided better results.

## 4.4 Evaluating a model

## 4.5 Visualising the outcome of a model (exploratory)
The model is 

[Back to top](https://github.com/MaartenPJ/ADS-portfolio#ads-portfolio-maarten-de-jonge)

# 5 Domain Knowledge
I have decided not to do the chapter Domain Knowledge.

[Back to top](https://github.com/MaartenPJ/ADS-portfolio#ads-portfolio-maarten-de-jonge)

# 6 Data Preprocessing
## 6.1 Data exploration
In the beginning, the research question was a different one, namely "Is it possible to detect eating and drinking sounds from audio using machine/deep learning?" Early Data exploration of the new/final dataset revealed very clear patterns in several of the eating and drinking sounds, e.g. recognisable and comparable bands in spectrograms [as seen here](https://github.com/MaartenPJ/ADS-portfolio/blob/main/Images/Drinking%20sound%20clear%20bands.png). The bands in this image correspond to 3 clear slurping sounds in the audio. Patterns like this strengthened our confidence, and led to the hypothesis, that it was indeed possible using neural networks..\
Further data exploration included plots and tables to explore the length of each file and the distribution of lengths and labels among samples in the dataset.\
There were no clear outliers, as our data was not numerical in the traditional sense.

Several examples of scripts for visualisations used in data exploration are collected in [this notebook](https://github.com/MaartenPJ/ADS-portfolio/blob/main/notebooks/Data%20Visualisation.ipynb)

## 6.2 Data cleansing
The data was not cleaned, because we were not certain what we were looking for, so passing it through for example a low-pass noise reduction filter could remove the relevant identifiers the models should be looking for.\
Furthermore, the Google Audioset contained mostly samples that had very little static/noise, so reducing this was not nescessary.\
Later, during data enhancement, more background noises were even added to make the samples more like a realistic recording from the teddy bear.

## 6.3 Data preparation
After the initial exploration of the dataset, we noticed the positive samples for both eating and drinking made up only a small percentage of the dataset. We decided to enlarge the amount of samples using data augmentation. To ensure the models would train on the data, not the augmentations, the same enhancements were performed on the negative samples.\
This work was largely done by Florian, with me providing help where asked.


## 6.4 Data explanation
The dataset consists of audio files taken from Google databases (mostly YouTube). Since most of these files were at a length of approximately 10 seconds, all files were made to be exactly 10 seconds long.\
The name of the dataset used is [Google AudioSet](https://research.google.com/audioset/). It contains millions of snippets of audio labeled with a description of their contents. These labels include things like vacuuming, breathing, several musical instruments, wind, clapping, knocking on door and silence, but most relevantly chewing and drinking.


## 6.5 Data visualisation (exploratory)
In order to better understand the nature of our datasets, several types of data visualisation were employed, listed below with scripts.\
To understand the dataset as a whole, we made a histogram of labels. I was unfortunately unable to find this. I suspect it was deleted from the server at some point.\
To get more insight into individual datapoints, we made a waveform, an MFCC and a (mel)spectrogram of them.\
I compiled several scripts used to visualise data into [this notebook](https://github.com/MaartenPJ/ADS-portfolio/blob/main/notebooks/Data%20Visualisation.ipynb).
These visualisations were done mostly using the numpy, pandas, wave, MatPlotLib, librosa and soundfile libraries.

[Back to top](https://github.com/MaartenPJ/ADS-portfolio#ads-portfolio-maarten-de-jonge)

# 7 Communication
## 7.1 Presentations
I presented 3 internal presentations, of which 1 alone and 2 with another member of the group.\
I also presented 2 external presentations, of which 1 alone and 1 with another group member.\
Here are two examples of presentations I gave: [an external presentation](https://github.com/MaartenPJ/ADS-portfolio/blob/main/presentations/External%20Presentation%2010_12.pptx) and [an internal presentation](https://github.com/MaartenPJ/ADS-portfolio/blob/main/presentations/Internal%20Presentation.pptx).\
Most of the feedback I recieved regarding my presentations was positive. I alledgedly speak clearly and fluently in English and am quite good at getting the information across.

## 7.2 Writing paper
The paper can be found [here](https://github.com/MaartenPJ/ADS-portfolio/blob/main/Paper/ResearchPaperNourish.pdf).\
I, together with Lucas, laid down the structure for the paper.\
In the paper I wrote the chapters Introduction, Model evaluation, Conclusion, Recommendations.\
I also contributed to the chapter Dataset (Data augmentation).\
I standardised the references (both to literature and to figures) and the formatting and performed the final spelling check.\
I also helped the other members of my team with questions about scientific writing.

[Back to top](https://github.com/MaartenPJ/ADS-portfolio#ads-portfolio-maarten-de-jonge)
