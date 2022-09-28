
## FedFOR
FedFOR: Stateless Heterogeneous Federated Learning with First-Order Regularization, https://arxiv.org/abs/2209.10537  

We derive a first-order gradient regularization to penalize inconsistent local updates due to local data heterogeneity. Specifically, to mitigate weight divergence, we introduce a first-order approximation of the global data distribution into local objectives, which intuitively penalizes updates in the opposite direction of the global update. The end result is a stateless FL algorithm that achieves 1) significantly faster convergence (i.e., fewer communication rounds) and 2) higher overall converged performance than SOTA methods under non-IID data distribution. Importantly, our approach does not impose unrealistic limits on the client size, enabling learning from a large number of clients as is typical in most FL applications.
