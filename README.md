# Computational Statistics

Labs from the [Master MVA](https://www.master-mva.com/cours/computational-statistics/) **Computational Statistics** class, taught by Prof. Stéphanie Allassonnière. 
Each lab assignment explores a core topic in statistical estimation and bayesian inference, combining theoretical derivations with practical Python simulations.

## TP1. Estimators and SGD Algorithm

In a first exercise, we compare two estimators for the uniform model $\mathcal{U}([0,\theta])$: the method-of-moments estimator and the maximum likelihood estimator (MLE). 
The MLE is shown to have a stricyly lower quadratic risk for $n\ge 2$.

In the second part, we implement the **Stochastic Gradient Descent (SGD)** algorithm from scratch to learn a linear classifier, then studies how observation noise degrades estimation quality.

<p align="center"><img height="300" alt="visualization_tp1" src="https://github.com/user-attachments/assets/b69ebce4-97af-4d85-b888-9ff1bb07d1cd" /></p>

Finally, the method is applied to the [UCI Heart Disease dataset](https://archive.ics.uci.edu/dataset/45/heart+disease), reaching >70% accuracy.

## TP2. EM Algorithm for GMMs

This second practical work is centered on parameter estimation of a **Gaussian Mixture Model (GMM)** using the **Expectation-maximization (EM) algorithm**. 
We first implement a way to sample from a GMM, and then implement the EM algorithm in this particular setting.

<p align="center">
<img height="250" alt="visualization_tp2_1" src="https://github.com/user-attachments/assets/a6950c02-d563-4815-99c0-bfe79e31d82f" />
<img height="250" alt="visualization_tp2_2" src="https://github.com/user-attachments/assets/da2ca9d0-72d7-4615-ac38-94d7b2d8384e" />
</p>

## TP3. Hasting-Metropolis and Gibbs Samplers

In the first exercise, we study a hierarchical population model for longitudinal data, such as disease progression measurements, and we try to estimate the model's parameters.
Because direct sampling from the posterior is not possible, we implement the **Stochastic Approximation EM (SAEM)** algorithm using a **Metropolis-Hastings (MH)** sampler for the latent variables. 

The second exercise explores Data Augmentation, using **Markov chain Monte Carlo (MCMC)**. We construct a bivariate Markov chain and use a Gibbs sampler to approximate a specific density.

<p align="center"><img height="300" alt="visualization_tp3_1" src="https://github.com/user-attachments/assets/3a542ad1-d89c-430f-80f6-15b8cc750dba" /></p>

## TP4. Improving the Metropolis-Hastings Algorithm

In this final practical work, we explore advanced techniques to overcome common limitations of the standard MH algorithm.
First, we tackle the difficulty of tuning the proposal distribution's parameters by implementing an Adaptive MH within Gibbs sampler. 
This algorithm automatically adjusts the variances of the proposal distributions on the fly to target an optimal acceptance rate.

Next, we address the challenge of sampling from highly multimodal distributions, where standard MCMC often gets stuck in a single local mode.
We demonstrate this failure on a toy target distribution defined as a mixture of 20 well-separated Gaussians
To solve this, we implement **Parallel Tempering**, which runs multiple Markov chains in parallel at varying "temperatures".
This allows to improve exploration, and then to correctly sample from the target distribution.

<p align="center"><img height="250" alt="visualization_tp4_1" src="https://github.com/user-attachments/assets/19557652-22c2-4c18-b56d-718f0c4b1e0d" /></p>



