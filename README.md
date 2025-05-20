# Autoregressive Neural Processes

![image](https://github.com/user-attachments/assets/9f2977a8-93b4-4b38-b850-25079a78b72f)

In this report, we replicate the experiments from the paper Autoregressive Conditional Neural Pro-
cesses [1], compare our results to those presented in the original work, and extend the study. The paper
introduces an autoregressive (AR) inference procedure for Neural Processes (NP), with a particular fo-
cus on Conditional Neural Processes (CNP). This approach addresses a key limitation of standard NP
architectures, which often struggle to capture dependencies between outputs in joint predictions.

The experiments we replicate from the original work include synthetic regression tasks and Sim-to-
Real transfer using Lotka-Volterra dynamics.

Beyond replication, we explore several extensions of the autoregressive inference framework:
* Application to image data: We investigate the performance of Convolutional Conditional Neu-
ral Processes (ConvCNP) and Autoregressive Convolutional Conditional Neural Processes (AR
ConvCNP) on image datasets, specifically the Extended Modified National Institute of Standards
and Technology (EMNIST) dataset for image completion [2]. These experiments aim to evaluate
whether data with strong local correlations, such as pixel intensities in images, benefit from AR
inference.
* AR inference in Latent Bottleneck Attentive Neural Processes (LBANP): We adapt the LBANP
to incorporate the AR inference mechanism. Our goal is to determine whether similar performance
improvements are observed when applying the AR regime.
* AR Inconsistency: We explore a limitation in the AR inference strategy: the resulting joint distri-
bution over targets depends on their ordering, violating permutation consistency. To address this,
we investigate alternative approaches to obtain a more robust and order-agnostic estimate of the
joint target distribution.

*[1] W. P. Bruinsma, S. Markou, J. Requiema, A. Y. Foong, T. R. Andersson, A. Vaughan, A. Buonomo,
J. S. Hosking, and R. E. Turner, “Autoregressive conditional neural processes,” arXiv preprint
arXiv:2303.14468, 2023.*

*[2] G. Cohen, S. Afshar, J. Tapson, and A. Van Schaik, “Emnist: Extending mnist to handwritten
letters,” in 2017 international joint conference on neural networks (IJCNN), pp. 2921–2926, IEEE,
2017.*
