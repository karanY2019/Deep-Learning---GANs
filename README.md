# Deep Learning - GANs
Compare different choices of losses in GAN training.

## MSE loss

## Wasserstein GAN (WGAN)
WGAN is proposed to address the vanishing gradient problem in the original GAN loss
when the discriminator is way ahead of the generator. One thing to change in WGAN
is that the output of the discriminator should be now ‘unbounded’, namely you need to
remove the sigmoid function at the output layer. And you need to clip the weights of the
discriminator so that their L1 norm is not bigger than c.

I tried c from the set {0.1, 0.01, 0.001, 0.0001} and compare the difference from the MSE loss.

## Least Square GAN

It provides a smoother loss surface than the original GAN loss (MSE loss)
 
Training curves and the generated samples:

