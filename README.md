# watchmyset

The goal of this project was to create a laughter detector for stand-up comedy sets, such that it can statistically breakdown the number of laughs in a set, percentage of laughs, and plot the timepoints where a comedian got laughs. 

To do so, I trained a recurrant neural network on around ~20 stand-up comedy sets available on YouTube. These sets were chunked into 1 second .wav files, totalling about ~6000 .wav files, and hand-labeled for whether there was laughter. Each second was converted into its Mel-frequency Cepstral Coefficient (MFCC), essentially a mathematical transformation that converts a noisy .wav into a 99x13 set of features that somewhat approximates the way that the human ear breaks down sound. I then trained my long-term short-memory model on this data. 

This trained model can then be used to reasonably detect laughter in stand-up comedy sets it hadn't been trained on. 

All the code in this project was written on ran on [Google Colaboratory](https://research.google.com/colaboratory/faq.html). 

The Google Colab notebook for training the model is located in this repo, named `WMS_train_model.ipynb`. (Suggested to open in Colab)

The Google Colab notebook for detecting laughter in YouTube videos is located in this repo, named `WMS_predict_YT.ipynb`. (Suggested to open in Colab). This is also listed as a .py file called `predict.py`.

Currently working on putting this up as a website, for comedians to paste a link to their sets and immediately seeing laughter statistics on it. 

The dataset the model was trained can be downloaded here: https://drive.google.com/open?id=1hyINuRXl6QXOPwLZIDjNbThiTsCxOMpv

And the labeled CSVs corresponding to the above dataset can be downloaded here: https://drive.google.com/open?id=1cTRqzzFFzoC9QgOZ5OKecSgf8ROar5c7


