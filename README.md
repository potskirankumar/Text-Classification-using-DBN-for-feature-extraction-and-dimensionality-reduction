# Text-Classification-using-DBN-for-feature-extraction-and-dimensionality-reduction
#The dataset I used was downloaded from Kaggle.

About the project:


When we are talking with our friends, relatives or some people, we can express positive and negative expressions. Let’s say, you are giving a bad review about a product, that’s the negative sentiment. If you are giving a good word or review, then that’s positive sentiment.

Sentiment is nothing but the view or opinion or thought about something. Sentiments can be positive, negative, etc.

In this article, I am presenting you a sentiment analysis system. In this, Word2Vec is used for text representation (embedding). And then, feed to DBN and then the last output is fed to SGDCLassifier to classify the sentiments. So, we are building an NLP sentiment analysis model.


Sentiment analysis is a process of identifying or classifying whether a text is positive, negative, neutral or other sentiments (opinions, etc.). Sentiment analysis in NLP is the contextual meaning of text to help an organization or group of people to understand what the opinions are, given by other people about something (may be product).

Nowadays, on social media platforms or e-commerce site or any other sites, a large group of people give comments or talk about something. So, this can be identify as sentiments using a sentiment analysis system.

Sentiment analysis is important because we can understand what people opinions are expressing.

Deep Belief Network:
Before we learn about Deep Belief Networks (DBN), there are some things we need to understand. However, let me explain only the theory parts in short.

First is the Boltzmann Machine:

Boltzmann Machine was invented by Geoffrey Hinton and Terry Sejnowski in 1985. It is a neural network that has interconnections between neurons to make stochastic decisions and also an unsupervised generative deep learning model. This machine has two layers, one is visible or input layer and another one is hidden layer.

Let’s talk briefly about Boltzmann Machine.

The Boltzmann Machine has a system of units (neurons) that are interconnected and whose state is determined probabilistically. It learns the distribution over data by adjusting weights and biases of the connections. The neurons or units are stochastic in nature means they are activated based on probabilities which is determined by the network’s current state. In Boltzmann Machine an energy function is used to represents the likelihood of the system’s configuration. The visible layer is responsible to observe the data and the hidden layer is based on visible layer. Between the two layers, the network tries to minimize the energy function.

After this, let’s talk about Restricted Boltzmann Machine (RBM).

RBM is a variant of Boltzmann Machine. But here the interconnections between neurons are not available. The connections are only between visible layer and hidden layer. The visible layer works as input layer. The hidden layer captures features that explain the data and it consists of binary units, and number of hidden units is the one that determines the model’s capacity to capture complex patterns. The visible and hidden layers are connected via weights.

There is forward pass that the visible layer accepts inputs and hidden layer captures the latent features. The activation probability of hidden layer is determined using the input from the visible layer and the weights. Once the hidden units are activated, the visible units are reconstructed by performing reverse process. Since there is not output layer in RBM, through reconstruction the visible layer is constructed through hidden layer. This is done by using Contrastive Divergence algorithm. This algorithm is used to minimize the difference between the original data and the reconstructed data. The weights are updated here.

Now let’s talk about Deep Belief Network (DBN).

DBN is unsupervised deep learning model that can be used in feature extraction and dimensional reduction, and was invented by Geoffrey Hinton and his group in 2006. DBN is multi-layered networks and also a sophisticated Artificial Neural Network. Each layer is the RBM. DBN has stack of RBMs. DBN can be used to discover and find patterns within a large dataset. Each RBM has visible layer and hidden layer. Visible layer acts as an input layer and the output from the hidden layer accepts as input in another RBM. Means, the output of one RBM is used as input of another RBM and the final output of the top layer is used for classification or regression. DBN follows greedy learning, means each RBM gets trained independently.

Implementation of Sentiment Analysis:
#prefer the code
