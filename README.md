# 2018 Fall-W210-Capstone
# Emergent
*Samir Datta, Thu Nguyen and Yubo Zhang*


Webpage:  https://goldenmonster0602.github.io/w210final.github.io/

**Introduction**

This repository contains the files needed for our capstone project website. Additionally, we have included the code used to create an interactive application in the folder /full_app_files. The goal of this project was to create visualizations to allow developers to more easily detect and search for issues based on the content of their app reviews. For more information and background on the project, as well as interactive examples, please visit the project website listed above.

**Data**

Our data comprises of over 164,000 pre-processed reviews, acquired and used with permission from the ReMine-Lab (2). The reviews come from apps in both the iOS and Google Play store: NOOA Radar, YouTube, Viber, Clean Master, Ebay, and Swiftkey. Included along with the review text is information about the rating, version number, and more. 


**Lessons Learned**

For this project, we used Latent Dirichlet Allocation (LDA), which is an algorithm used to discover the topics that are present in a corpus of words. Uniform Manifold Approximation and Projection (UMAP) is a dimension reduction technique that can be used for visualisation. similar with t-SNE.  We also incorporated with Word2Vec, which computes vector representations of words, to help us visualize topics over time. There were a few methods that we tried that ended up not working as well as the ones listed above:


*K-means cluster*: The K-means clustering algorithm is used to find groups which have not been explicitly labeled in the data and to find patterns and make better decisions. However it didn't work with our data.

*PCoA*: Principle Coordinate Analysis is a method to explore and to visualize similarities or dissimilarities of data. It starts with a similarity matrix or dissimilarity matrix and assigns for each item a location in a low-dimensional space. By using PCoA we can visualize individual and/or group differences. However, PCoA didn't work for us. Here is the image of the cluster that we generated.

![alt text](https://github.com/samird121/w210-app-review-capstone/blob/master/new_scraped_reviews/pcoa.png)

[PCoA Page](https://github.com/samird121/w210-app-review-capstone/blob/master/new_scraped_reviews/YuboClusteringtesting.ipynb)

*Word2Vec alternatives such as Doc2Vec, Sense2Vec*

Doc2Vec and Sense2Vec are extensions on the Word2Vec methodology that attempt to model more sophisticated relationships, such as document-level vector representations beyond simply averaging the word vectors, or different vectors for the same word with different meanings. We attempted to implement them but found the models did not perform well due to the nature of the review data, including its messiness, wide variety of length, and sparsity. More sophisticated word embeddings require more data and ideally cleaner data, and we ultmately decided that Word2Vec was suitable for the goals of our project.



**Reference**
1. Topic Modeling: https://medium.com/nanonets/topic-modeling-with-lsa-psla-lda-and-lda2vec-555ff65b0b05
2. Gao, C., Zeng, J., Lyu, M., & King, I. "Online App Review Analysis for Identifying Emerging Issues." *Proceedings of the 40th International Conference on Software Engineering,* 2018
3. Hu, M. & Liu, B. "Mining and Summarizing Customer Reviews." *Proceedings of the ACM SIGKDD International Conference on Knowledge Discovery and Data Mining (KDD-2004)*, Aug 22-25, 2004, Seattle, Washington, USA
4. Kalyanam, J., Mantrach, A., Saez-Trumper, D., Vahabi, H. & Lanckriet, G. "Leveraging Social Context for Modeling Topic Evolution." *Proceedings of the 21th ACM SIGKDD International Conference on Knowledge Discovery and Data Mining,* Aug 10-13, 2014, Sydney, NSW, Australia
