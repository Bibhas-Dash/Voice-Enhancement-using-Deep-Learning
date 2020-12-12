# Voice-Enhancement-using-Deep-Learning

Here I have attempted to design a DL pipeline for audio enhancement. This is basically a DNN based filter that takes real world audio as input and removes noises to produce a clean audio.

# Introduction:

While dealing with real time audio speech signals, we are always concerened about the various types of noises that are added to the original signal which results in corruption of the original clean signal. In order to retrieve a better quality signals, it is essential to enhance these signals by eliminating the noises present in them. Here this process is attempted to achieve through Deep Learning. 

# Dataset:

The dataset used for this project is a curated dataset taken from NOIZEUS speech corpus,a noisy speech corpus. The noisy database contains 30 IEEE sentences (produced by three male and three female speakers) corrupted by eight different real-world noises at different SNRs. The noise was taken from the AURORA database and includes suburban train noise, babble, car, exhibition hall, restaurant, street, airport and train-station noise. Here the sentences were originally sampled at 25 kHz and downsampled to 8 kHz. 
Used dataset: https://drive.google.com/drive/folders/1y-_HbXrJMKo0QXlTRNTmGOuZU1ntsW2i?usp=sharing

# Downloadable link for the dataset:

You can find the complete dataset here https://ecs.utdallas.edu/loizou/speech/noizeus/

# Approach taken:

* Used a fully connected network with 5 hidden layers with 1000 hidden units each for speech denoising.
* tanh activation functions are used for the hidden layers, inspired from http://paris.cs.illinois.edu/pubs/liu-interspeech2014.pdf
* Xavier initialization has been used for weights along with batch normalization and Adam Optimizer.
* relu activation function is used for the last layer, due to non negative output requirement and to avoid vanishing gradient problem.
* 30% dropouts are applied during training to avoid overfitting.

# Frameworks:

Tensorflow

# References:

Liu, D. & Smaragdis, P. & Kim, Minje. (2014). Experiments on deep learning for speech denoising. Proceedings of the Annual Conference of the International Speech Communication Association, INTERSPEECH. 2685-2689.http://paris.cs.illinois.edu/pubs/liu-interspeech2014.pdf 

Hu, Yi & Loizou, Philipos. (2007). Subjective comparison and evaluation of speech enhancement algorithms. Speech communication. 49. 588-601. 10.1016/j.specom.2006.12.006. http://www.utdallas.edu/~loizou/cimplants/quality_spcom07.pdf

# Note:

#The results of the current model is not yet optimized and subject to further regressions in future.
