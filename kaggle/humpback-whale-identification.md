感觉：有些方法对这个组没用但是对另一个组有用，说明感觉是很主观的，或者有些方法之间有互斥。

## Knowledge collection

[face recognition survey](https://so.csdn.net/so/search/s.do?q=%E4%BA%BA%E8%84%B8%E8%AF%86%E5%88%AB%E7%B3%BB%E5%88%97&t=blog&u=Fire_Light_)

https://zhuanlan.zhihu.com/p/34044634
summary of all kinds of loss functions based on softmax loss used in face recognition, including ArcFace

https://zhuanlan.zhihu.com/p/34404607

https://zhuanlan.zhihu.com/p/34436551

very good, worthy of reading again

[ArcFace](https://arxiv.org/pdf/1801.07698.pdf)
similar to SphereFace and CosFace

[Chinese](https://blog.csdn.net/u014380165/article/details/80645489)

https://zhuanlan.zhihu.com/p/33750684

https://zhuanlan.zhihu.com/p/33288325



## Summary of viable methods
https://www.kaggle.com/c/humpback-whale-identification/discussion/82437

some other guys summary

1. augmentation methods

* HorizontalFlip
* Rotate with 16 degree limit
* ShiftScaleRotate with 16 degree limit
* RandomBrightnessContrast
* RandomGamma
* Blur
* Perspective transform: tile left, right and corner
* Shear
* MotionBlur
* GridDistortion
* ElasticTransform
* Cutout

2. Loss functions
* ArcFace
* CosFace
One-shot Face Recognition by Promoting Underrepresented Classes

3. small images to bigger images
4. easy pairs to harder pairs
5. flip images to make new classes

## 1st place
[Link to disscussion](https://www.kaggle.com/c/humpback-whale-identification/discussion/82366)

[Chinese](https://zhuanlan.zhihu.com/p/58496385)

4-channel, RGB + Mask


## 3rd place
[Link to disscussion](https://www.kaggle.com/c/humpback-whale-identification/discussion/82484)

bbox + landmark

ArcFace

mix aligned and non-aligned images




## 5th place

[Link to discussion](https://www.kaggle.com/c/humpback-whale-identification/discussion/82369)

[Link to summary](https://weiminwang.blog/2019/03/01/whale-identification-5th-place-approach-using-siamese-networks-with-adversarial-training/)

*architecture:* Siamese Network

*tricks:*
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

## 9th place
https://www.kaggle.com/c/humpback-whale-identification/discussion/82427

some experiences:
* After several competitions I begin to realise that sometimes when you don’t have much data light encoders may really boost your score. Like they don’t tend to overfit much to rare classes and label noise. This is just a hypothesis that need to be carefully verified.

augmentaion methods and augmentation libraries

## 10th place
[Link](https://www.kaggle.com/c/humpback-whale-identification/discussion/82430)

## 15th place
[Link](https://www.kaggle.com/c/humpback-whale-identification/discussion/82361)
* over sampling
* sphereface
* multi-layer fusion

I used global average pool to each layer(layer 1- 4) and concatenated them.
* image alignment

## 24th place
[Link](https://www.kaggle.com/c/humpback-whale-identification/discussion/82359)

* Martin's solution train longer
* Training for another 5-10 epochs resulted in a similar score but the distribution of predicted whales was much more variable though the scores remained very close. I figured this was due to randomness in how the augmentations were applied so I trained several dozen versions of this model with minor variations--changing image size from 224 up to 600 both grayscale and rgb.

## 31th place
* Marin's solution
* RGB
* Pretrained model
* bigger size

## 57th place
[Link](https://www.kaggle.com/c/humpback-whale-identification/discussion/82364#latest-481830)
Good use of fastai

## 143th place
[Link](https://www.kaggle.com/c/humpback-whale-identification/discussion/82480)
famous Radek code
