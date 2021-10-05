# Sentiment analysis of IMDB dataset using BERT Fine-tuning
A deep neural network for sentiment classification task of IMDB Review Dataset.


Libraries used: PyTorch and Transformers


## PREREQUISITE: DATASET

To run the notebook in Google Colab, we need to load the dataset in the google drive.

1. Download the hw1_muskan.zip
2. Decompress the zip and download the 'imdb dataset' folder
3. Go to your drive.google.com
4. Click on New and then Upload folder
5. Select the 'imdb dataset' folder from your local drive to upload

During mounting of google drive and loading the dataset, google might ask to enter access token.
Please do so by clicking on the link shown on running the cell and pasting it in the box created there to continue running the code.

## USAGE

### Method 1: USE THE BEST MODEL FOR F-SCORE AND PREDICTION

1. Download the best model from hw1_model_muskan.zip and mount it on your google drive in 'My Drive'
2. Please run sections: 
    1. *1. Install required libraries and load the data*
    2. *2. Defining Model architecture*
    
    Skip the section *3. Fine-tuning BERT* to avoid training the model from scratch
    
3. Go to section *4. Make Predictions* and run it to see the F-score on test/train/eval sets


### Method 2: RUN THE ENTIRE NOTEBOOK AGAIN: RE-TRAIN THE MODEL

1. Download the hw1_muskan.zip
2. Decompress the zip and download the sentiment-analysis.ipynb
3. Open https://colab.research.google.com/ in a web browser where there is google sign-in
4. Click on Upload tab and upload the sentiment_analysis.ipynb downloaded just now
5. From the drop-down menu, click on Runtime
6. Choose 'Change runtime type'
7. Click on Hardware accelarator drop down and choose GPU/TPU
8. Click Save
9. From the drop-down menu, click on Runtime again
10. Choose Run All
11. The notebook will take 5+ hours to run, please wait till it finishes or save weights after one epoch and then resume on some other day
OR
10. Go to the top most cell
11. Press Shift+Enter to execute the cell and move to the next cell
12. Again press Shift+Enter to execute the next cell and continue doing the same till the end
13. Note: Training and evaluating in the Fine-tuning BERT section will take more time to run


## LIMITATIONS
* Due to limitations of RAM and memory on Google Colab, the notebook will take time to fine-tune BERT and predict on the dataset given.
* BERT is a large model with a lot of parameters, so fine-tuning it takes time.
* F1-score of the model is dependent on the batch_size and max_seq_len hyperparameters chosen for our model. These two fields are currently constrainted  via resources accessible on Google Colab.


## NOTE

* The Colab Notebook is divided into sections based on the overall steps taken: Install required libraries and load the data, Define model architecture, Fine-tuning BERT, Make Predictions.
* Please find the explanation of each step in Text cell before the code cell and/or in comments within each code cell
