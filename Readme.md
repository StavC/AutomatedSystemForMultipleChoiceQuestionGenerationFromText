This Project and Paper were authored by Stav Cohen, Avitay Geltman, and Doron Battino.

This marks our inaugural endeavor in undertaking a project of such magnitude and composing a scientific paper in ACL format. Despite encountering numerous challenges along the way, the journey proved immensely rewarding.

We successfully developed a robust MCQ model. We invite readers to explore our paper and discover opportunities for further advancement.








# Abstract 

Automatic multiple choice question (MCQ) generation is a useful yet challenging task in Natural Language Processing. It is the task of automatic generation of context–dependent questions and answers, where for a given context, a corresponding question is provided along with a set of answers of which solely one is correct. Automation is of great interest due to the tedious process of manual constructing tests of this type. Therefore, researchers have been putting effort into this automation task since the late 1990’s. In our study, we present an innovative Transformer based system automatically generating MCQs for a given text. Our system is constructed of three separate units that fulfill different tasks. The goal of the first is to provide answers from a given context to the second. Consequently, the latter generates questions based on the provided answers and corresponding contexts. The third unit receives all the above and generates relevant false answers. A transformer based model was trained to distinguish between generated and non–generated answers, resulting in a F1 score of 43–59%, meaning our generated answers were essentially undistinguishable. Additional metrics further demonstrated prosperity of the answer generation unit. For the question generation task, the commonly used BLEU–4 metric was utilized, obtaining a decent score of 14.76 upon integration of a smoothing function. Finally, in terms of the generated false answers’ quality, plausible and diverse candidates were successfully obtained. Many of which presented a proper grammatical structure, consistency with the context, and reasonable logic.
![image](https://user-images.githubusercontent.com/26565498/160733754-97f1aac2-64ef-47a0-a8c3-b71f0647b6bc.png)
# This repository is divided to 4 folders:


The folder SQuAD1.1JSONS contains two JSON files utilized during the model training phase.
Train Notebooks comprises three notebooks: AnswerGenerationTrain, DistractorGenerationTrain, and QuestionGenerationTrain, each housing the training scripts for our three models.
Metric Notebooks, namely AnswerGenerationMetrics and QuestionGenerationMetrics, encompass the scripts utilized to evaluate the performance of the AnswerGeneration and QuestionGeneration models.
Additionally, a CSV file titled "Further examples on Wikipedia pages" showcases the final output of our system on selected contexts sourced directly from Wikipedia pages. The generation of MCQs was facilitated by executing the notebook @AQD_FullNotebookDemo.ipynb on several texts.
A demonstration script named 'AQD_FullNotebookDemo.ipynb' is available within the repository. This notebook presents the end-to-end pipeline of our models, integrating all three models seamlessly. It enables the generation of MCQs from the SQuAD dataset or custom text inputs.

To access the weights of the three models, training is required using the provided training notebooks. Alternatively, we can facilitate the process by uploading the weights to a cloud storage upon request.

For further inquiries, please reach out to us at {cohenstav1, avitaygl, doronbatt}@gmail.com
