# MRI_Neural_Segmentation
In this notebook we are implementing a U-net type of Neural Network for Image segmentation over a dataset of mri images with its correspondent masks for tumor segmentation. This dataset is provided via kaggle API, this dataset (Segmentation masks for FLAIR abnormality approved by a board-certified radiologist at Duke University) can be found in this website: https://wiki.cancerimagingarchive.net/display/Public/TCGA-LGG.

![imagen](https://user-images.githubusercontent.com/18196870/201544171-48c70900-0929-4d51-880e-b1e8ae546cac.png)

In the notebook as well, we are going to train 3 models with similar network architecture with different methods to achieve some results in this image segmentation task.

- Model 1 -> In this model we are going to train our architecture with the arrenged dataset we are given from different patients, so, the mri of some patients are going to be splited for training and other, for test and validation. In this case, we use dropout as our main regularization method and the loss we are going to use is a keras loss named binary crossentropy, a vanilla loss for the keras library, which we are going to use for the classification of every pixels in two classes, normal or tumor.

- Model 2 -> In this model we are going to train our architecture with the dataset shuffled, so the mri images are shuffled in a uniform manner, and then we will split the images for training, validation and test subsets. Our main regularization method is dropout, and the loss we are going to use is a custom loss named Jaccard, which is used in statistics.

- Model 3 -> In this model we are going to train our architecture with the dataset shuffled, so the mri images are shuffled, in the same way as the previous case. Our main regularization method is the data augmentation we are going to apply to our training image dataset, and the loss we are going to use is a custom loss named Jaccard, which is the same as the used in the previous case.
