# AMD-CR

This is an open-source aesthetic mixed dataset with classification and regression called AMD-CR, which we completed in the [Victory team of Besti](https://www.victory-lab.net/).

In order to construct an aesthetic dataset with reasonable distribution and high quality of aesthetic annotation, we filter and reconstruct a dataset called AMD-CR. There are two datasets in AMD-CR: aesthetic mixed dataset with classification (AMD-C) applied to the binary classification training task, and aesthetic mixed dataset with regression (AMD-R) applied to the regression task.

### Construction of AMD-CR
The part of AMD-CR comes from image aesthetic benchmark datasets: DPChallenge, Photo.net, AVA [1], CUHKPQ [2] and SPAQ [3], AVA and DPChallenge come from www.dpchallenge.com. Photo.net is from www.photo.net; another part comes from self-built datasets: GLAMOUR, OUTDOOR, NG and PSA. GLAMOUR is from www.glamour-photos.org, OUTDOOR is from www.outdoor-photos.com, NG is from www.dili360.com, PSA is from www.psachina.org. We collected the high-quality data by downloading high-quality on the professional photography websites. We obtain a portion of the public images from these websites and integrate them into our aesthetic dataset. We distribute continuous labels to [0, 10.0] through standardized fractional labelling and map binary labels to 0 and 1. 0 represents the images with low aesthetic quality and 1 represents the images with high aesthetic quality. Discrete datasets only have binary labels, while continuous datasets both have binary labels and continuous labels. We focused on selecting images of high and low quality, and we performed a preliminary selection of the images with general aesthetic quality to balance the data distribution. The constitution of AMD-CR is shown in the table below.

### Construction of AMD-R
We filter the data with the continuous labels in AMD-CR. The images of low and high segments with the scores less than 4.0 points or more than 6.0 points are reserved, and the middle segment images (4.0-6.0) are randomly sampled. Then we get 59,371 images from AMD-R.

### Construction of AMD-C
We removed the images ranging between 4.0 points and 6.0 points in the AMD-CR to ensure that the ratio of positive and negative samples is 1:1. Finally, we obtain AMD-C containing 61,660 images.

[1] N. Murray, L. Marchesotti, and F. Perronnin, “Ava: A large-scale database for aesthetic visual analysis,” in 2012 IEEE Conference on Computer Vision and Pattern Recognition. IEEE, 2012, pp. 2408–2415.

[2] W. Luo, X. Wang, and X. Tang, “Content-based photo quality assessment,” in 2011 International Conference on Computer Vision. IEEE, 2011, pp. 2206–2213.

[3] Y. Fang, H. Zhu, Y. Zeng, K. Ma, and Z. Wang, “Perceptual quality assessment of smartphone photography,” in Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition, 2020, pp.3677–3686.

*************************************************************************************
### The constitution of AMD-CR.

| Datasets      | Volume     | labels  |
| ---------- | :-----------:  | :-----------:  |
| DPChallenge + AVA     | 61461     |  Continuous    |
| Photo.net     |  29690     | Discrete    |
| NG     | 4140     | Discrete    |
| SPAQ     |  4102     | Continuous    |
| PSA     |  3460     | Discrete    |
| GLAMOUR     |  2701     | Discrete    |
| OUTDOOR     |  1916     | Discrete    |

**PS: Considering the copyright of images, we will only open-source the picture number public.**
  
### Our Paper  
  
Xin Jin, Hao Lou, Huang Heng, Xinning Li, Xiaodong Li, Shuai Cui, Xiaokun Zhang, Xiqiao Li. 
Pseudo-labelling and Meta Reweighting Learning for Image Aesthetic Quality Assessment. IEEE Transactions on Intelligent Transportation Systems (T-ITS) **[arXiv](https://arxiv.org/abs/2201.02714)**(2201.02714)

