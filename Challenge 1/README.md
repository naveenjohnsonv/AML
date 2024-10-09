## Challenge 1: Aerial Imagery

### Completion requirements

#### Overview

To assess the impact of climate change on Earth's flora and fauna, it is vital to quantify how human activities such as logging, mining, and agriculture are impacting our protected natural areas. Researchers in Mexico have created the VIGIA project, which aims to build a system for autonomous surveillance of protected areas. A first step in such an effort is the ability to recognize the vegetation inside the protected areas. In this competition, you are tasked with creation of an algorithm that can identify a specific type of cactus in aerial imagery.

This is a competition that has been inspired by an existing competition on Kaggle.

#### Acknowledgments

This is an original competition defined [here](https://www.kaggle.com/competitions/aerial-cactus-identification/data).

**References:**

Efren López-Jiménez, Juan Irving Vasquez-Gomez, Miguel Angel Sanchez-Acevedo, Juan Carlos Herrera-Lozada, Abril Valeria Uriarte-Arcia, Columnar Cactus Recognition in Aerial Images using a Deep Learning Approach. Ecological Informatics. 2019.

Acknowledgements to Consejo Nacional de Ciencia y Tecnología. Project cátedra 1507. Instituto Politècnico Nacional. Universidad de la Cañada. Contributors: Eduardo Armas Garca, Rafael Cano Martnez and Luis Cresencio Mota Carrera. J.I. Vasquez-Gomez, JC. Herrera Lozada. Abril Uriarte, Miguel Sanchez.

### Dataset Description

This dataset contains a large number of 32 x 32 thumbnail images containing aerial photos of a columnar cactus (Neobuxbaumia tetetzo). Images have been from the original dataset to make them uniform in size. The file name of an image corresponds to its id.

You must create a classifier capable of predicting whether an images contains a cactus.

#### Files

- `train/` - the training set images
- `test/` - the test set images (you must predict the labels of these)
- `train.csv` - the training set labels, indicates whether the image has a cactus (has_cactus = 1)

The `sample_submission.csv` file is currently not used: it is a sample submission file in the correct format, that is used in automatic evaluation platforms such as Kaggle. You can discard this file.

**Original approaches:** do not hesitate to go crazy! What about using an existing "Visual Question Answering" LLM model to "synthetically label" the files in the test directory? Why not! Try!!

**ATTENTION:** you can download the full dataset from my [Kaggle dataset page](https://www.kaggle.com/datasets/michiard/aerial-cactus). There you just have to click the download button. The advantage of using the Kaggle dataset page is that it allows you visually navigate the data. Alternatively, I have also uploaded a zip with the files here on Moodle.

### Metrics

For this challenge, you are required to define an appropriate metric. You face a binary classification problem, but at this stage you do not know if your data is balanced. Throughout your work, especially the data analysis part, you will first need to characterize your data, and then come up with a valid performance metric to assess the quality of your model. 

**Important note:**
Where are my labels? You will notice that the test set (clearly) has no labels! This is used in a "real world" challenge, whereby you are asked to predict labels for unseen data during training. Labels are "kept secret" by the challenge organizers, and the automatic evaluation system uses the submission file (ID, predicted lables) to compare to the "secret ground truth".

Since we will not have this step in the AML course, you are tasked with the important goal of splitting your training set, and hold out validation and test data to check the performance of your model.
