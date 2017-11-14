# Using a VAE-based low-dimensional parameterization to solve inverse problems with complex geologic prior information

This Python 2.7 package contains the (1) convolutional variational autoencoder (VAE) and (2) DREAM<sub>(ZS)</sub> Markov chain Monte Carlo (MCMC) sampler
used for probabilistic inversion of hydrologic data within complex binary geological media by [Laloy et al. (2017)](https://doi.org/10.1016/j.advwatres.2017.09.029).

## Large data files

Because of Github space limits, neither the training sets (of geologic model realizations) nor the trained VAE models (needed to reproduce the results presented in the paper) 
are provided herein. But these are of course available. Please drop me an email if you want to get these files. 

## Building the VAE-based representation

The codes for training our VAEs with Theano/Lasagne are contained in vaecnn2D_train.py (for the two 2D considered case studies) and vaecnn3D_train.py 
for the two 3D considered case studies). Also, realizations generated by the trained VAE models can be produced by running the model_generation.py script.

Note that since the development of Theano has just stopped, I am planning to rewrite the code in Tensorflow/Keras. Just need time :-).

## Performing the inversion

To perform the MCMC inversion within the VAE latent space using DREAM<sub>(ZS)</sub>, use the run_mcmc.py script from the Inversion folder.

## Citation

Please make sure to cite our paper if you use any of the contained code in your own projects or publication: 

Eric Laloy, Romain Hérault, John Lee, Diederik Jacques, Niklas Linde, Inversion using a new low-dimensional representation 
of complex binary geological media based on a deep neural network, Advances in Water Resources, 2017, 110:387-405.

## License

Licence: the Theano/Lasagne code for the VAE is under MIT license while the MCMC inversion code is under GPL license. See the corresponding folders for details.

## Contact

Eric Laloy (elaloy@sckcen.be) 