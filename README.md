# skin-cancer
Skin Cancer classifier, final solution pipeline:

Image -> Deep clustering backbone -> PCA(256 dims) -> HDBScan -> nth_cluster classifier -> answer.
(nx256x265x3) -> (nx10.000) -> (nx256) -> (nx n_clusters); (nx256x256x3) & nth_clustes -> (nx(lession_qty+1))


Deep clustering: 

Backbone: efficientnetB4 ó resnet18. Imagenet pretrained.
Dataset: HAMM10000 = 10.000 images.

Fitting:
1) Backbone inference on all dataset
2) PCA fit and transform
3) HDBScan fit and transform
4) Dataset and pseudo labels train & test split.
5) Backbone fitting
6) repeat.

(paper https://research.fb.com/publications/deep-clustering-for-unsupervised-learning-of-visual-features/)
