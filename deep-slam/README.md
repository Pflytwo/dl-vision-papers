#### Contents  
- [SLAM](#slam)
- [Dynamic SLAM](#dynamic-slam)
- [VO](#vo)
- [VIO](#vio)

------

------

#### SLAM

##### Fusion++
[Fusion++: Volumetric Object-Level SLAM](https://arxiv.org/abs/1808.08378)&nbsp;[2017 arXiv]

##### Deep SLAM
[Toward Geometric Deep SLAM](https://arxiv.org/abs/1707.07410)&nbsp;[2017 arXiv]

##### CNN-SLAM
[CNN-SLAM: Real-time dense monocular SLAM with learned depth prediction](https://arxiv.org/abs/1704.03489)&nbsp;[2017 CVPR]

##### PAD 
[Probabilistic Data Association for Semantic SLAM](https://www.cis.upenn.edu/~kostas/mypub.dir/bowman17icra.pdf)&nbsp;[2017 ICRA]

##### Semi-Dense 3D Semantic Mapping
[Semi-Dense 3D Semantic Mapping from Monocular SLAM](https://arxiv.org/abs/1611.04144)&nbsp;[2016 arXiv]

##### SemanticFusion
[SemanticFusion: Dense 3D Semantic Mapping with Convolutional Neural Networks](https://arxiv.org/abs/1609.05130)&nbsp;[2017 ICRA]

------

#### Dynamic SLAM

深度学习可以识别场景的各个物体，现在利用深度学习来求解动态场景SLAM问题的工作也越来越多了；

##### MID-Fusion
[MID-Fusion: Octree-based Object-Level Multi-Instance Dynamic SLAM](https://arxiv.org/abs/1812.07976)&nbsp;[2018 arXiv]

##### DS-SLAM
[DS-SLAM: A Semantic Visual SLAM towards Dynamic Environments](https://arxiv.org/abs/1809.08379)&nbsp;[2018 IROS]

------

#### VO

##### RegNet
[RegNet: Learning the Optimization of Direct Image-to-Image Pose Registration](https://arxiv.org/abs/1812.10212)&nbsp;[2018 arXiv]

##### SIVO
[Self-Improving Visual Odometry](https://arxiv.org/abs/1812.03245)&nbsp;[2018 arXiv]

##### MagicVO
[MagicVO: End-to-End Monocular Visual Odometry through Deep Bi-directional Recurrent Convolutional Neural Network](https://arxiv.org/abs/1811.10964)&nbsp;[2018 arXiv]

> 1. 这里使用Bi-LSTM，不仅利用前面帧的信息，同时还利用的后面帧的信息（整体和[DeepVO](#deepvo)有点类似）；
> 2. 这里使用Bi-LSTM求解VO，虽然Bi-LSTM能利用前后帧信息，但是在实际使用过程，后面的帧图像无法预先获得；

##### VSO
[VSO: Visual Semantic Odometry](https://demuc.de/papers/lianos2018vso.pdf)&nbsp;[2018 ECCV]

##### LS-VO
[LS-VO: Learning Dense Optical Subspace for Robust Visual Odometry Estimation](https://arxiv.org/abs/1709.06019)&nbsp;[2018 ICRA]&nbsp;[code: [keras](https://github.com/isarlab-department-engineering/LSVO)]

> 1. 在光流结果上利用CNN压缩特征，利用该特征再去求取relative pose；

##### UnDeepVO 
[UnDeepVO: Monocular Visual Odometry through Unsupervised Deep Learning](https://arxiv.org/abs/1709.06841)&nbsp;[2018 arXiv]&nbsp;[[project page](http://senwang.gitlab.io/UnDeepVO/)]

> 1. 利用已知baseline的双目图像去非监督学习depth(这个也是非监督学习depth的经典做法)；
> 2. 利用上面求解的depth约束前后帧图像photometric一致性以及前后帧3d几何关系一致性，这样loss确定，可以非监督去求解relative pose；

##### DeepVO 

[DeepVO: Towards End-to-End Visual Odometry with Deep Recurrent Convolutional Neural Networks](https://arxiv.org/abs/1709.08429)&nbsp;[2017 ICRA]&nbsp;[[project page](http://senwang.gitlab.io/DeepVO/)] 

> 1. 前后帧拼接企图特征；
> 2. 特征利用LSTM向后传递，使用两次LSTM；

------

#### VIO

##### VINet
[VINet: Visual-Inertial Odometry as a Sequence-to-Sequence Learning Problem](https://arxiv.org/abs/1701.08376)&nbsp;[2017 AAAI]
