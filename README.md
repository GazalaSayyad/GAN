# GAN
Generate fake images of MNIST dataset



Generative Adversarial Network (GAN)
Generative Adversarial Networks (GANs) are a powerful class of neural networks that are used for unsupervised learning. It was developed and introduced by Ian J. Goodfellow in 2014. GANs are basically made up of a system of two competing neural network models which compete with each other and are able to analyze, capture and copy the variations within a dataset.


Generative Adversarial Networks (GANs) can be broken down into three parts:
1.Generative: To learn a generative model, which describes how data is generated in terms of a probabilistic model.
2.Adversarial: The training of a model is done in an adversarial setting.
3.Networks: Use deep neural networks as the artificial intelligence (AI) algorithms for training purpose.




The generative model captures the distribution of data and is trained in such a manner that it tries to maximize the probability of the Discriminator in making a mistake. The Discriminator, on the other hand, is based on a model that estimates the probability that the sample that it got is received from the training data and not from the Generator.
The GANs are formulated as a minimax game, where the Discriminator is trying to minimize its reward V(D, G) and the Generator is trying to minimize the Discriminator’s reward or in other words, maximize its loss. It can be mathematically described by the formula below:

                              min max V( D, G )
                              G    D
                              

where,
G = Generator
D = Discriminator
Pdata(x) = distribution of real data
P(z) = distribution of generator
x = sample from Pdata(x)
z = sample from P(z)
D(x) = Discriminator network
G(z) = Generator network
So, basically, training a GAN has two parts:

Part 1: The Discriminator is trained while the Generator is idle. In this phase, the network is only forward propagated and no back-propagation is done. The Discriminator is trained on real data for n epochs, and see if it can correctly predict them as real. Also, in this phase, the Discriminator is also trained on the fake generated data from the Generator and see if it can correctly predict them as fake.
Part 2: The Generator is trained while the Discriminator is idle. After the Discriminator is trained by the generated fake data of the Generator, we can get its predictions and use the results for training the Generator and get better from the previous state to try and fool the Discriminator.
The above method is repeated for a few epochs and then manually check the fake data if it seems genuine. If it seems acceptable, then the training is stopped, otherwise, its allowed to continue for few more epochs.


Different types of GANs:
1. Vanilla GAN
2.Conditional GAN (CGAN)
3.Deep Convolutional GAN (DCGAN)
4.Laplacian Pyramid GAN (LAPGAN)
5.Super Resolution GAN (SRGAN)
