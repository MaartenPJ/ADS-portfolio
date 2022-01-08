## ADS-portfolio Maarten de Jonge Student number 17113571

# DataCamp Course
From the DataCamp Courses, I completed the following:
-
-
-

Screenshots of the statements of accomplishment can be found here [#insert link]

# Reflection and Evaluation
- own contribution
- learning objectives
- group project as a whole

# Research Project
- task definition
Our group was one of three to work for the Smart Teddy Project under supervision of Hani Al-Ers. This project aims to help in the care of elders with beginning cases of dementia by introducing a teddy bear in their home that uses sensors to monitor their quality of life.
Our group, "Team Nourish", was tasked with finding an algorithm that can distinguish eating (and less importantly drinking) sounds from ambient/background/other sounds around the house.
Our chosen research question was "Which deep learning model is optimal to detect eating and drinking sounds from audio?"
Furthermore, after talking with the problem owner, we decided to define "optimal" as a high accuracy score, but with a secondary emphasis on precision. This is because the problem owner would rather have the teddy bear miss a meal and have a caretaker check up an additional time (False Negative), than the teddy reporting meals that didn't happen, potentially resulting in a malnourished senior.
The reason accuracy was chosen as the leading metric despite the wish for high precision, was that focussing on accuracy during training resulted in a better overall model.

- evaluation
In future studies about this problem, I would advise more research into applying binary classifiers. We unfortunately didn't have enough time to spend on this avenue until the very end of the project, due to the fact that we only had half of our initial group for most of the project.
Despite not spending much time and effort though, the binary models were quite promising and certain binary classifiers even outperformed their multiclass classifier equivalents in certain specific metrics.
[insert more recommendations here]

- conclusions
[more here]
Unfortunately our best individual result was with a ResNet transfer learning model, but due to the incredible fluctuations between epochs on all these models, we could not confidently recommend any of these models as the optimal model. We concluded, that the ResNet models we trained were too unreliable.
[more here]

- planning
Our group has used Scrum in the planning of this project. We made a Scrum board on Jira and ended up with over a hundred total tickets.

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
