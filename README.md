# Bayesian mixture of Gaussians

NumPy implementation of Coordinate Ascent Variational Inference for the Bayesian mixture of Gaussians model (Section 10.2 of Bishop's PRML).

Below is a run of the algorithm on the Old Faithful dataset. Iteration 0 means right after initialization without any learning. For each cluster: 

- The transparency of the red color represents the expected value of its mixing coefficient under the Dirichlet posterior. 
- The contour represents the 50% contour of the Gaussian parametrized by the mean (which includes both a cluster mean and a cluster covariance) of the Gaussian-Wishart posterior.

At iteration 200, the expected mixing coefficients are zero except for two clusters.

Do note that the clusters I obtained seem to be less concentrated (i.e., have "higher variance") than the ones obtained in the original text. This could be due to different prior hyperparameters since the original text doesn't give the values of the prior hyperparameters it used.

![](/pngs/iter_0.png) | ![](/pngs/iter_1.png) | ![](/pngs/iter_5.png) | ![](/pngs/iter_200.png)
:-------------------------:|:-------------------------:|:-------------------------:|:-------------------------:|
