# Deep Learning - GANs
Wasserstein GAN, Least Square GAN and Conditional GAN
Compare different choices of losses in GAN training. (Fashion-Mnist dataset)

## Wasserstein GAN (WGAN)

WGAN is proposed to address the vanishing gradient problem in the original GAN loss
when the discriminator is way ahead of the generator. One thing to change in WGAN
is that the output of the discriminator should be now ‘unbounded’, namely you need to
remove the sigmoid function at the output layer. And you need to clip the weights of the
discriminator so that their L1 norm is not bigger than c.

I tried c from the set {0.1, 0.01, 0.001, 0.0001} and compare the difference from the MSE loss.

## Least Square GAN

It provides a smoother loss surface than the original GAN loss (MSE loss)

# Conditional GAN

To generate not just any images from FashionMNIST data distribution, but images with a particular label such as shoes. This is called the Conditional GAN because now samples are drawn from a conditional distribution given a label as input.

