## Gini index:
{ Gini Index }=1-\sum_{j}{ }_{\mathrm{j}}^{2} 
1. Gini Index is a metric to measure how often a randomly chosen element would be incorrectly identified.
2. It means an attribute with lower gini index should be preferred.

## Latent Space:
1. The latent space is simply a representation of compressed data in which similar data points are closer together in space.
2. Latent space is useful for learning data features and for finding simpler representations of data for analysis.
3. We can understand patterns or structural similarities between data points by analyzing data in the latent space, be it through manifolds, clustering, etc.
4. We can interpolate data in the latent space, and use our model’s decoder to ‘generate’ data samples.
5. We can visualize the latent space using algorithms such as t-SNE and LLE, which takes our latent space representation and transforms it into 2D or 3D.

## Inception Score:
1. It is an objective metric for evaluating the quality of generated images, specifically synthetic images output by generative adversarial network models.
2. The inception score has a lowest value of 1.0 and a highest value of the number of classes supported by the classification model.
3. The calculation of the inception score on a group of images involves first using the inception v3 model to calculate the conditional probability for each image (p(y|x)). The marginal probability is then calculated as the average of the conditional probabilities for the images in the group (p(y)).
4. The KL divergence is then calculated for each image as the conditional probability multiplied by the log of the conditional probability minus the log of the marginal probability.
5. KL divergence = p(y|x) * (log(p(y|x)) – log(p(y)))
6. The KL divergence is then summed over all images and averaged over all classes and the exponent of the result is calculated to give the final score.


## SSIM: https://medium.com/srm-mic/all-about-structural-similarity-index-ssim-theory-code-in-pytorch-6551b455541e
1.The Structural Similarity Index (SSIM) metric extracts 3 key features from an image:
* Luminance -  Luminance is measured by averaging over all the pixel values.
* Contrast - It is measured by taking the standard deviation (square root of variance) of all the pixel values.
* Structure-  The structural comparison is done by using a consolidated formula but in essence, we divide the input signal with its standard deviation so that the result has unit standard deviation which allows for a more robust comparison.
2. A value of +1 indicates that the 2 given images are very similar or the same while a value of -1 indicates the 2 given images are very different.
![image](https://user-images.githubusercontent.com/40149518/146059869-1ee763fb-3a02-43d5-9e81-6f91f2141880.png)

### Notes:
For image quality assessment, it is useful to apply the SSIM index locally rather than globally. First, image statistical features are usually highly spatially nonstationary. Second, image distortions, which may or may not depend on the local image statistics, may also be space-variant. Third, at typical viewing distances, only a local area in the image can be perceived with high resolution by the human observer at one time instance (because of the foveation feature of the HVS [49], [50]). And finally, localized quality measurement can provide a spatially varying quality map of the image, which delivers more information about the quality degradation of the image and may be useful in some applications.
