# Awesome Autoencoder for Representation Learning
*Last updated on August, 2020.*  
<br>

## Introduction
The **bottlenecked** nature empowered autoencoder-based models (AEs) the ability to learn features of input data; the **unsupervised** and 
**generative nature** of AEs further facilitate the generalizability of the learned features, which is particularly useful in the scenario when unlabeled data is abundant whereas labeled data is scarce.  

Down to a science, the future of machine learning to solve real-world tasks is likely to be generative models (to pretrain) followed by discriminative models (to predict). AEs (especially its variational families), as an important member of generative models, thus becomes crucial to study.  
 
In this curated list of literature review, we will focus on recent (1) theories to understand the learning ability and characteristics of autoencoders, (2) models and applications exploiting autoencoders for representation learning and downstream tasks, and (3) adversarial attacks and defenses for autoencoders. We may also include some not so autoencoder relavant but representation learning relavant papers in this list.   

The list is organized as follows:  
- [Survey](#Survey)  
- [Theory](#Theory)  
- [Models](#Models) 
- [Applications](#Applications) (Here we are specifically interested in applications using encoder outputs for downstream task.)    
- [Attacks on Autoencoders](#Attacks)   
- [Defense by Autoencoders](#Defenses)  
- [Miscellaneous](#Miscellaneous)  

In each section, papers are primarily organized by topic, then by conferences, lastly by chronological order. A short summary will be accompanied below the paper if necessary. 🧑🏻‍🚀 denotes important papers from my own perspective. 🐣 refers to the ones I haven't read but they look interesting, and would be added a summary below later. 
<br>

## Survey
**Recent Advances in Autoencoder-Based Representation Learning** [[link](https://arxiv.org/abs/1812.05069)]    
Michael Tschannen, Olivier Bachem, Mario Lucic  
*3rd workshop on Bayesian Deep Learning (NeurIPS 2018)*   
<br>

**Threat of Adversarial Attacks on Deep Learning in Computer Vision: A Survey** [[link](https://ieeexplore.ieee.org/abstract/document/8294186)]   
Naveed Akhtar, Ajmal Mian  
*IEEE Access, 2018*  
<br>


## Theory
🧑🏻‍🚀 **Disentangling Adversarial Robustness and Generalization** [[link](https://openaccess.thecvf.com/content_CVPR_2019/html/Stutz_Disentangling_Adversarial_Robustness_and_Generalization_CVPR_2019_paper.html)]  
David Stutz, Matthias Hein, Bernt Schiele  
*CVPR, 2019*   
> This papers shows that for a data manifold:  
> 1. There are generally two types of adversarial examples: **off-manifold** and **on-manifold**. 
> 2. **On-manifold** adversarial examples are generalization errors, and on-manifold adversarial training improves generalization.  
> 3. Regular robutsness and generalization are not contradicting.  
<br>

**Guess First to Enable Better Compression and Adversarial Robustness** [[link](https://arxiv.org/abs/2001.03311)]  
Sicheng Zhu, Bang An, Shiyu Niu  
*Information Theory and Machine Learning Workshop, NIPS, 2019*  
> This paper shows that better compression ($I(X; Z)$) and less label information ($I(Z; Y)$) improves adversarial robustness. This two properties can be useful in designing robust AEs for downstream tasks.    
<br>

🧑🏻‍🚀 **Towards a Theoretical Understanding of the Robustness of Variational Autoencoders** [[link](https://arxiv.org/abs/2007.07365)]  
Alexander Camuto, Matthew Willetts, Stephen Roberts, Chris Holmes, Tom Rainforth  
*Preprint, 2020*  
> This paper provides a general metric to evaluate the robustness of probabilitic models: $r$-robustness.  
> - Specifically, it shows that we are able to define a region which which any perturbation will produce a reconstruction similar to the original reconstruction.
<br>

## Models
**World Models** [[link](https://arxiv.org/abs/1803.10122)] [[website](https://worldmodels.github.io/)] [[talk](https://www.youtube.com/watch?v=HzA8LRqhujk&feature=youtu.be)]     
David Ha, Jürgen Schmidhuber  
*NIPS, 2018*  
> One of the greatest paper in NIPS. Its subtitle is: *Can Agents Learn Inside of Their Own Dreams?*  
> The World Model can be conceived as this two-stage process:  
> 1. Learn a **compressed** representation of the environment in an **unsupervised manner**;  
> 2. Use the learned representation to train a policy to solve downstream tasks.
<br>

**From Variational to Deterministic Autoencoders** [[link](https://openreview.net/forum?id=S1g7tpEYDS)] [[code](https://github.com/ParthaEth/Regularized_autoencoders-RAE-)]  
Partha Ghosh, Mehdi S. M. Sajjadi, Antonio Vergari, Michael Black, Bernhard Scholkopf  
*ICLR, 2020*  
<br>

**Provably robust deep generative models** [[link](https://arxiv.org/abs/2004.10608)]  
Filipe Condessa, Zico Kolter  
*Preprint, 2020*  
<br>

## Applications
**Variational Autoencoder for Semi-supervised Text Classification** [[link](https://arxiv.org/abs/1603.02514)]  
Weidi Xu, Haoze Sun, Chao Deng, Ying Tan  
*AAAI, 2017*  
<br>

**Deep Patient: An Unsupervised Representation to Predict the Future of Patients from the Electronic Health Records** [[link](https://www.semanticscholar.org/paper/Deep-Patient%3A-An-Unsupervised-Representation-to-the-Miotto-Li/18c39ba04333d31c6cb10faf79d1f18692c38d0f)]  
R. Miotto, Li Li, B. Kidd, J. Dudley  
*Scientific Reports, 2016*  
> This paper uses a 3-layer denoising autoencoder to learn representations for raw EHR data.
<br>

**Semi-Supervised Learning of the Electronic Health Record for Phenotype Stratification** [[link](https://www.sciencedirect.com/science/article/pii/S153204641630140X)]  
Brett K. Beaulieu-Jonesab, Casey S. Green  
*Journal of Biomedical Informatics, 2016*  
> This paper uses the enoising autoencoder with the random forest classifier to predict survival rates of patients.
<br>

**Representation Learning with Autoencoders for Electronic Health Records: A Comparative Study** [[link](https://arxiv.org/abs/1801.02961)]  
Najibesadat Sadati, Milad Zafar Nezhad, Ratna Babu Chinnam, Dongxiao Zhu  
*Preprint, 2019*  
> This paper gives a general framework of using autoencoder to extract features of EHR data, then build prediction models on top of them.
<br>

## Attacks
**Adversarial Images for Variational Autoencoders** [[link](https://arxiv.org/abs/1612.00155)] [[code](https://github.com/tabacof/adv_vae)]  
Pedro Tabacof, Julia Tavares, Eduardo Valle  
*PAdversarial Training Workshop (NIPS, 2016)*  
<br>

**Adversarial Attacks on Variational Autoencoders** [[link](https://arxiv.org/abs/1806.04646)]   
George Gondim-Ribeiro, Pedro Tabacof, Eduardo Valle   
*CoRR, 2018*  
<br>

**Adversarial Examples for Generative Models** [[link](https://ieeexplore.ieee.org/abstract/document/8424630/)]  
Jernej Kos, Ian Fischer, Dawn Song  
*IEEE S&P Workshops, 2018*  
> Provides 3 different schemes resulting in reconstruction change. 
<br>

**Constructing Unrestricted Adversarial Examples with Generative Models** [[link](https://arxiv.org/abs/1805.07894)] [[code](https://github.com/ermongroup/generative_adversary)]  
Yang Song, Rui Shu, Nate Kushman, Stefano Ermon  
*NIPS, 2018*  
<br>

**When Deep Fool Meets Deep Prior: Adversarial Attack on Super-Resolution Network** [[link](https://scholar.google.com/scholar_url?url=https://dl.acm.org/doi/abs/10.1145/3240508.3240603%3Fcasa_token%3DmVORIJYgzAMAAAAA:xEcap40LdiR67ExAX_Fw4RPCEOIEVS6iyt7jpLpNcpwWNfpQqBYbEISJpKGdCKUhLAdYsqoLdwpYsQ&hl=en&sa=T&oi=gsb&ct=res&cd=0&d=9750722567383918778&ei=5m4yX_ewIbuB6rQPkoaAuAc&scisig=AAGBfm1V9jZxniRZjaQDzvt_iilCt1Je9g)]  
Minghao Yin, Yongbing Zhang, Xiu Li, Shiqi Wang  
*Proceedings of the 26th ACM international conference on Multimedia (MM, 2018)*   
<br>

**Adversarial Out-domain Examples for Generative Models** [[link](https://ieeexplore.ieee.org/abstract/document/8802456/?casa_token=5pJGy5iWsJgAAAAA:z10cWZLFJOM-ArPQgnMsWOueed-0OqhGxLziBxmLjjqMVRdJnzIaJ1AIoL0kk9YN1bPHi8twbQ)]   
D. Pasquini, M. Mingione, M. Bernaschi  
*IEEE European Symposium on Security and Privacy Workshops (Euro S&PW, 2019)*  
<br>

🐣 **Towards Feature Space Adversarial Attack** [[link](https://arxiv.org/abs/2004.12385)]   
Xu Q, Tao G, Cheng S, Tan L, Zhang X.  
*Preprint, 2020*   
<br>

🐣 **Type I Attack for Generative Models** [[link]](https://arxiv.org/abs/2003.01872)  
Chengjin Sun, Sizhe Chen, Jia Cai, Xiaolin Huang  
*Preprint, 2020*   
> One example attack on VAE by this paper is that the proposed attack can change an original image significantly to a meaningless one but their reconstruction results are similar. 
<br> 

🐣 **On Breaking Deep Generative Model-based Defenses and Beyond** [[https://proceedings.icml.cc/static/paper_files/icml/2020/2236-Paper.pdf](link)]  
Yanzhi Chen, Renjie Xie, Zhanxing Zhu  
*ICML, 2020*  

## Defenses  
**Deep Variational Information Bottleneck** [[link](https://arxiv.org/abs/1612.00410)]  
Alexander A. Alemi, Ian Fischer, Joshua V. Dillon, Kevin Murphy  
*ICLR, 2017*  
<br>

**Adversarial Defense of Image Classification Using a Variational Auto-Encoder** [[link](https://arxiv.org/abs/1812.02891)]   
Yi Luo, Henry Pfister  
*Preprint, 2018*  
<br>

**Are Generative Classifiers More Robust to Adversarial Attacks?** [[link](https://openreview.net/forum?id=BkVmRByPG)]   
Yingzhen Li   
*Rejected by ICLR Workshop, 2018*   
> This paper is more on the robustness of bayes classifiers compared to deterministic classifiers.  
> - Notably, it applies generative modeling (variational inference) to improve original bayes classifers.  
> - It implies that, generative models may fascilitate gradient masking which in turn become more robust to attacks. The stochastic nature of generative models may play an important role for gradient masking.
<br>

**Sufficient Conditions for Robustness to Adversarial Examples: a Theoretical and Empirical Study with Bayesian Neural Networks**  [[link](https://openreview.net/forum?id=B1eZRiC9YX)]  
*Rejected by ICLR Workshop, 2019*   
Yarin Gal, Lewis Smith  
> This paper proves, under two sufficient conditions, that idealised models can have no adversarial examples.
<br>

🧑🏻‍🚀 **Improving VAE's Robutsness to Adversarial Attacks** [[link](http://www.robots.ox.ac.uk/~twgr/assets/pdf/willetts2020disentangling.pdf)]  
M Willetts, A Camuto, S Roberts, C Holmes  
*Preprint, 2019*  
> This paper introduces a hierarchical VAE which can improve adverarial robustness while preserving reconstruction ability.  
> - This idea is based on the observation that disentangled representation improves robustness yet reducing the quality of reconsturction ability.
<br>

**Certified Robustness to Adversarial Examples with Differential Privacy**  [[link](https://arxiv.org/abs/1802.03471)]  
Mathias Lecuyer, Vaggelis Atlidakis, Roxana Geambasu, Daniel Hsu, Suman Jana  
*Preprint, 2019*  
> This paper provides a defense which could be done in the feature space (by adversarial smoothing).
<br>

**Evaluating Robustness of Deep Image Super-Resolution Against Adversarial Attacks** [[link](http://openaccess.thecvf.com/content_ICCV_2019/html/Choi_Evaluating_Robustness_of_Deep_Image_Super-Resolution_Against_Adversarial_Attacks_ICCV_2019_paper.html)]   
J. Choi, H. Zhang, J. Kim, C. Hsieh, J. Lee   
*ICCV, 2019*   
<br>

**Resisting Adversarial Attacks Using Gaussian Mixture Variational Autoencoders** [[link](https://www.aaai.org/ojs/index.php/AAAI/article/view/3828)]   
Partha Ghosh, Arpan Losalka, Michael J. Black  
*AAAI, 2019*
<br>

**Defense-VAE: A Fast and Accurate Defense Against Adversarial Attacks** [[link](https://link.springer.com/chapter/10.1007/978-3-030-43887-6_15)]   
Xiang Li, Shihao Ji   
*PKDD, 2019*  
> This paper uses VAE to purge adversarial perturbations from contaminated images, and shows this preprocessing can help defend both white-box and black-box attacks.
<br>

**Bridging Adversarial Robustness and Gradient Interpretability** [[link](https://arxiv.org/abs/1903.11626)]   
Beomsu Kim, Junghoon Seo, Taegyun Jeon  
*Safe Machine Learning Worshop of ICLR, 2019*  
> - This papers shows that adversarial training makes gradients more interpretable. 
> - It also shows that there is a trade-off between test accuracy and gradient interpretability.
> - It then provides ways to mitigate this trade-off.
<br>

🧑🏻‍🚀 **Adversarially Robust Representations with Smooth Encoders** [[link](https://openreview.net/forum?id=H1gfFaEYDS)]  
Taylan Cemgil, Sumedh Ghaisas, Krishnamurthy (Dj) Dvijotham, Pushmeet Kohli  
*ICLR, 2020*  
<br>

**Evaluating the Robustness of Defense Mechanisms based on AutoEncoder Reconstructions against Carlini-Wagner Adversarial Attacks** [[link]](https://septentrio.uit.no/index.php/nldl/article/view/5173)   
Petru Hlihor, Riccardo Volpi, Luigi Malagò   
*Proceedings of the Northern Lights Deep Learning Workshop, 2020*   
> Similar to the above one, this paper shows that reconstruction by autoencoders is an effective preprocessing approach on images to defend common adversarial attacks. 
<br>

**Double Backpropagation for Training Autoencoders against Adversarial Attack** [[link](https://arxiv.org/abs/2003.01895)]  
Chengjin Sun, Sizhe Chen, Xiaolin Huang  
*Preprint, 2020*  
> This paper proposes a training procedure to enhance the robustness of AEs.  
> - It is based on the observation that AEs are sensitive to inputs, i.e., one can slightly modify an input but has totally different codes.  
> - Therefore, the authors restrict gradients from the reconstruction image to the original one, making AEs less sensitive to small perturbation.
<br>

**Defending Adversarial Attacks via Semantic Feature Manipulation**  [[link](https://arxiv.org/abs/2002.02007)]  
Shuo Wang, Tianle Chen, Surya Nepal, Carsten Rudolph, Marthie Grobler, Shangyu Chen  
*Preprint, 2020*  
<br>

**ARAE: Adversarially Robust Training of Autoencoders Improves Novelty Detection**  [[link](https://arxiv.org/abs/2003.05669)]  
Mohammadreza Salehi, Atrin Arya, Barbod Pajoum, Mohammad Otoofi, Amirreza Shaeiri, Mohammad Hossein Rohban, Hamid R. Rabiee  
*Preprint, 2020*  
<br>

## Miscellaneous 
(*This section is not so relevant and can be skipped.*)  

**Perturbation Analysis of Learning Algorithms: A Unifying Perspective on Generation of Adversarial Examples** [[link](https://arxiv.org/abs/1812.07385)]  
Emilio Rafael Balda, Arash Behboodi, Rudolf Mathar  
*Preprint, 2018*  
<br>

**Robustness Analysis of Deep Neural Networks in the Presence of Adversarial Perturbations and Noisy Labels** [[link](https://www.ti.rwth-aachen.de/diss/Emilio_Rafael_Balda.pdf)]   
Emilio Rafael Balda Cañizares  
*Preprint, 2019*  
> This paper provides an information-theoretical view on learning with noisy labels.
<br>

**Protecting Against Image Translation Deepfakes by Leaking Universal Perturbations from Black-Box Neural Networks** [[link](https://arxiv.org/abs/2006.06493)]  
Nataniel Ruiz, Sarah Adel Bargal, Stan Sclaroff  
*Preprint, 2020*  
