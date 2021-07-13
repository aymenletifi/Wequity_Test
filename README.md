# Wequity_Test


In this notebook, I detailed how I went about the topic modelling of the ESG news dataset. <br><br>
Because of the lack of Data on the internet and because there is no labels, I opted with the unsupervised learning to perform this task.<br>
For the first step, I used regular LDA model with gensim library in two ways:<br>
<ul>
<li>The first one is using the title, content and description seperately to see if that gives us anything.</li>
<li>The second one is combine the title,content and description to have a huge corpus to use in the same LDA model.</li>
</ul>

Then, for the second step, I used Guided LDA model with a seed topic list that I created based on internet research about the ESG topics and based on the results of the previous LDA model.<br>
A small problem persisted with 2 topics, So I extracted the ambiguous data and performed another segmentation with the regular LDA model to separete between the last 2 topics.<br><br>

The final dataset can be found in this link: <https://drive.google.com/drive/folders/1rFk2TuRMLHHYl2V4F-5KnxhHkTI41VhG?usp=sharing>

### Conclusion:<br>
The second solution with the guided LDA model and then the regular LDA model seemed to work fine but there are other more precise and performant solutions out there like ESG-BERT which is a fine-tuned BERT model specifically for ESG topics prediction, BerTopic which is a model based on bert for topic modelling, and keyATM which is a model for keyword assisted topic modelling.
