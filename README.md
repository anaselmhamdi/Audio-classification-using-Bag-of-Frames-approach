
# Audio Classification using Bag-of-Frames approach

## Project Description 
Human speech can be broken down into elementary phonemes and can be modeled using algorithms like Hidden Markov Models (HMM). Stationary patterns like rhythm and melody can be used in classification of music. In contrast, Non speech sounds are random, unstructured, and lack the high level structures observed in speech and music, which makes it difficult to model them using HMM. In this project, the Bag of Frames approach is used to classify audio where a codebook of vectors is generated using K-Means clustering on the training data and  Bag of Frames for each of the audio clip is obtained using the codebook. These Bag of Frames are used as input to the classifiers for classification. 

The steps involved in the Bag of Frames approach for Environmental Sound Classification is described as follows: 


A.	Feature Extraction
    
    1. For the purpose of feature extraction, the audio clip is divided into several segments by choosing a particular window length.  
    2. Then features are extracted for each of the audio segment.
    3. Python libraries Librosa and Scikits are used to extract audio features like MFCC, delta MFCC, Linear Predictive Coding(LPC) coefficients along with other frequency domain features like Mel Spectrogram, Spectral Centroid, Spectral Bandwidth, Spectral Roll Off   and temporal domain features like Root Mean Square Error (RMSE) and Zero Crossing Rate. 
    
    
B.	K-Means Clustering and Codebook generation

    1. Once the features are extracted, the whole training and test data is divided into training and test dataset. 
    2. Feature scaling and normalization of training data is done accross each feature.
    3. The normalized training data is fed into K-Means clustering algorithm with the number of clusters usually much higher than the total number of classes and the cluster centroids are obtained for the normalized training set. 
    4. These cluster centroids form the codebook. 
