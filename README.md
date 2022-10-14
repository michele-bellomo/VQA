# Kaggle Competition: Visual Question Answering (VQA)

The challenge consisted in designing an algorithm to answer questions regarding the input figures, as in the following:

<img src="images/VQA_.png?raw=true" alt="drawing" width="900"/>

This problem is known as Visual Question Answering (VQA) and it is a task that combines Computer Vision with Natural Language Processing. 
More details about the competition are available at <a>https://www.kaggle.com/competitions/anndl-2020-vqa</a>.

I tackled the problem by designing a neural network made up of two functional units. The first, consisting of a Convolutional Neural Network (CNN), is in charge of the encoding of the images, while the second, consisting of Long Short-Term Memory blocks (LSTM), has the task of encoding the questions. The two encoded vectors are then concatenated together and finally fed to the layers designed to generate the output answers. 

Concerning the CNN part, I tested both neural networks implemented from scratch and architectures already trained on Imagenet, finally calibrated through fine tuning.
Regarding word embedding, I compared the performance of a costum embedding with the pre-trained embedding "GloVE". Finally, for the LSTMs, I implemented and compared both a bidirectional and a hierarchical structure.

The notebook "" contains the implementation of the network that presented the best results on validation and test sets, consisting of a VGG architecture, LSTM's with hierarchical structure and GloVe word embedding. 
