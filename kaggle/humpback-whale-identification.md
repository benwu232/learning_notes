感觉：有些方法对这个组没用但是对另一个组有用，说明感觉是很主观的，或者有些方法之间有互斥。


## 1st place
[Link to disscussion](https://www.kaggle.com/c/humpback-whale-identification/discussion/82366)

[Chinese](https://zhuanlan.zhihu.com/p/58496385)

4-channel, RGB + Mask


## 3rd place
[Link to disscussion](https://www.kaggle.com/c/humpback-whale-identification/discussion/82484)

bbox + landmark

[ArcFace](https://arxiv.org/pdf/1801.07698.pdf)

mix aligned and non-aligned images




## 5th place

[Link to discussion](https://www.kaggle.com/c/humpback-whale-identification/discussion/82369)

[Link to summary](https://weiminwang.blog/2019/03/01/whale-identification-5th-place-approach-using-siamese-networks-with-adversarial-training/)

architecture: Siamese Network
tricks:
* different size of images
* different pretrained or self-designed net architectures 

This turned out to be very useful in our final ensembled submission, because ImageNet models tend to learn very differently from self-design ConvNets that are trained from scratch, and ensembling ImageNets with customized CNNs gives quite a bit of boost on LB score. 

In fact, pretrained DenseNet121 was the best performing model, which scored 0.959 MAP5 score on both public and private LB. And our best self-design ConvNets from scratch scored 0.957 on public LB / 0.954 on private LB. Both reported scores are for single model inference using k-fold approach (details in below). 

Head model using [Martin's implementation](https://www.kaggle.com/martinpiotte/whale-recognition-model-with-score-0-78563), and bbox.

image augmentation is useful to prevent overfitting

hard pairs mining. First easy pairs, then harder and harder pairs.

bootstrapped method：One thing to highlight is that we are changing our pseudo labeled dataset every time we have got an improved version of model (e.g. LB 0.938 -> LB 0.950 -> LB 0.965, etc. ) And every time we changed our pseudo labelled test data from this new model, we will have to re-create a new split of k-folds. This is simply because the dataset has changed, so the split will also need to reflect that.

stacking

paper: [SE-Net, Squeeze-Excitation](https://arxiv.org/abs/1709.01507)

https://blog.csdn.net/u014380165/article/details/78006626

https://blog.csdn.net/Evan123mg/article/details/80058077


## 7th place
[Link to discussion](https://www.kaggle.com/c/humpback-whale-identification/discussion/82352)
enhanced version of Radek

Classification

center loss

[ring loss](https://arxiv.org/abs/1803.00130)






