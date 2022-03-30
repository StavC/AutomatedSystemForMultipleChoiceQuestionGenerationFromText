This Project and Paper were created by Stav Cohen, Avitay Geltman and Doron Battino

# Abstract 

Automatic multiple choice question (MCQ) generation is a useful yet challenging task in Natural Language Processing. It is the task of automatic generation of context–dependent questions and answers, where for a given context, a corresponding question is provided along with a set of answers of which solely one is correct. Automation is of great interest due to the tedious process of manual constructing tests of this type. Therefore, researchers have been putting effort into this automation task since the late 1990’s. In our study, we present an innovative Transformer based system automatically generating MCQs for a given text. Our system is constructed of three separate units that fulfill different tasks. The goal of the first is to provide answers from a given context to the second. Consequently, the latter generates questions based on the provided answers and corresponding contexts. The third unit receives all the above and generates relevant false answers. A transformer based model was trained to distinguish between generated and non–generated answers, resulting in a F1 score of 43–59%, meaning our generated answers were essentially undistinguishable. Additional metrics further demonstrated prosperity of the answer generation unit. For the question generation task, the commonly used BLEU–4 metric was utilized, obtaining a decent score of 14.76 upon integration of a smoothing function. Finally, in terms of the generated false answers’ quality, plausible and diverse candidates were successfully obtained. Many of which presented a proper grammatical structure, consistency with the context, and reasonable logic.

# This repository is divided to 4 folders:

1. SQuAD1.1JSONS is a folder that holds the the two Jsons that were used during the training phase of the models
2. Train Notebooks holds 3 notebooks: AnswerGenerationTrain, DistractorGenerationTrain and QuestionGenerationTrain. these notebooks contains the training scripts that were used to build up our 3 models.
3. Metric Notebooks: AnswerGenerationMetrics and QuestionGenerationMetrics represent the metrics scripts that were used to examine the AnswerGeneration and QuestionGeneration models.
4. Further exxamples on Wikipedia pages: couple of CSV files that contains the final output of our system on a texts that were taken directly from the Wikipedia pages. each CSV contains 20 MCQ that were generated by running the notebook @AQD_FullNotebookDemo.ipynb

you can find a a Demo script by name of 'AQD_FullNotebookDemo.ipynb' in the repository it self, this notebook represent the end to end pipeline of our models and string together all 3 models.
allowing us to easily generate MCQ on SQuAD data set or provide our own text and create MCQ directly from it.