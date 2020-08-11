# Awesome Autoencoder for Representation Learning

## Introduction
This is a curated list of recent literature on autoencoders for representation learning. The unsupervised and generative nature of autoencoder-based models makes them popular tools for representation learning (e.g. using VAE as the feature extractor). In this list, we will focus on (1) recent theories to understand the learning ability and characteristics of autoencoders, (2) models and applications exploiting autoencoders for representation learning, and (3) adversarial attacks and defenses for autoencoders (p.s. we may also include some not so autoencoder related papers in this third part).  
<br>

## Format
Papers are generally listed organized by different conferences in chronological order. A short summary is provided below each paper. 🧑🏻‍🚀 denotes important papers from my own perspective.  
<br>

## Categories
[Survey](#Survey)  
[Theory](#Theory)  
[Models](#Models)  
[Applications](#Applications)  
[Attacks on Autoencoders](#Attacks)   
[Defense by Autoencoders](#Defenses)  
[Miscellaneous](#Miscellaneous)
<br>

## Survey
**Recent Advances in Autoencoder-Based Representation Learning**  
Michael Tschannen, Olivier Bachem, Mario Lucic  
*3rd workshop on Bayesian Deep Learning (NeurIPS 2018)*  
[[link](https://arxiv.org/abs/1812.05069)]   
<br>

**Threat of Adversarial Attacks on Deep Learning in Computer Vision: A Survey**  
Naveed Akhtar, Ajmal Mian  
*IEEE Access, 2018*  
[[link](https://ieeexplore.ieee.org/abstract/document/8294186)]  
<br>


## Theory
**Disentangling Adversarial Robustness and Generalization**  
David Stutz, Matthias Hein, Bernt Schiele  
*CVPR, 2019*  
[[link](https://openaccess.thecvf.com/content_CVPR_2019/html/Stutz_Disentangling_Adversarial_Robustness_and_Generalization_CVPR_2019_paper.html)]  
> This papers shows that for a data manifold:  
> 1. There are generally two types of adversarial examples: **off-manifold** and **on-manifold**. 
> 2. **On-manifold** adversarial examples are generalization errors, and on-manifold adversarial training improves generalization.  
> 3. Regular robutsness and generalization are not contradicting.  
<br>

## Models
**From Variational to Deterministic Autoencoders**  
Partha Ghosh, Mehdi S. M. Sajjadi, Antonio Vergari, Michael Black, Bernhard Scholkopf  
*ICLR, 2020*  
[[link](https://openreview.net/forum?id=S1g7tpEYDS)] [[code](https://github.com/ParthaEth/Regularized_autoencoders-RAE-)]
<br>

## Applications
<br>

## Attacks
**Adversarial Images for Variational Autoencoders**  
Pedro Tabacof, Julia Tavares, Eduardo Valle  
*PAdversarial Training Workshop (NIPS, 2016)*  
[[link](https://arxiv.org/abs/1612.00155)] [[code](https://github.com/tabacof/adv_vae)]  
<br>

**Adversarial Attacks on Variational Autoencoders**   
George Gondim-Ribeiro, Pedro Tabacof, Eduardo Valle   
*Preprint, 2018*  
[[link](https://arxiv.org/abs/1806.04646)]   
<br>

**Adversarial Examples for Generative Models**  
Jernej Kos, Ian Fischer, Dawn Song  
*IEEE S&P Workshops, 2018*  
[[link](https://ieeexplore.ieee.org/abstract/document/8424630/)] 
> Provides 3 different schemes resulting in reconstruction change. 
<br>

**Constructing Unrestricted Adversarial Examples with Generative Models**  
Yang Song, Rui Shu, Nate Kushman, Stefano Ermon  
*NIPS, 2018*  
[[link](https://arxiv.org/abs/1805.07894)] [[code](https://github.com/ermongroup/generative_adversary)]  
<br>

**When Deep Fool Meets Deep Prior: Adversarial Attack on Super-Resolution Network**  
Minghao Yin, Yongbing Zhang, Xiu Li, Shiqi Wang  
*Proceedings of the 26th ACM international conference on Multimedia (MM, 2018)*   
[link]  
<br>

**Adversarial Out-domain Examples for Generative Models**  
D. Pasquini, M. Mingione, M. Bernaschi  
*IEEE European Symposium on Security and Privacy Workshops (Euro S&PW, 2019)*  
[link]  
<br>

**Towards Feature Space Adversarial Attack**   
Xu Q, Tao G, Cheng S, Tan L, Zhang X.  
*Preprint, 2020*   
[[link](https://arxiv.org/abs/2004.12385)]   
<br>

## Defenses  
**Are Generative Classifiers More Robust to Adversarial Attacks?**  
Yingzhen Li   
*Rejected by ICLR Workshop, 2018*   
[[link](https://openreview.net/forum?id=BkVmRByPG)]  
> - This paper is more on the robustness of bayes classifiers compared to deterministic classifiers. Notably, it applies generative modeling (variational inference) to improve original bayes classifers.  
> - It implies that, generative models may fascilitate gradient masking which in turn become more robust to attacks. The stochastic nature of generative models may play an important role for gradient masking.
<br>

**Evaluating Robustness of Deep Image Super-Resolution Against Adversarial Attacks**    
J. Choi, H. Zhang, J. Kim, C. Hsieh, J. Lee   
*ICCV, 2019*   
[[link](http://openaccess.thecvf.com/content_ICCV_2019/html/Choi_Evaluating_Robustness_of_Deep_Image_Super-Resolution_Against_Adversarial_Attacks_ICCV_2019_paper.html)]  
<br>

## Miscellaneous








