# Benchmarking Results

Indexed by datasets
+ [AmazonBooks](#amazonbooks)
+ [Yelp](#Yelp)
+ [Gowalla](#Gowalla)
+ Movielens1M
+ Movielens10M
+ AmazonElectronics

## AmazonBooks

### amazonbooks_x0 (without side features)
We use this dataset following the same data splitting and preprocessing as in [NGCF](https://github.com/xiangwang1223/neural_graph_collaborative_filtering) and [LightGCN](https://github.com/kuandeng/LightGCN). We download the preprocessed data from [here](https://github.com/kuandeng/LightGCN/tree/master/Data/amazon-book). The data statistics are summarized as follows:

|                | #Users | #Items | #Interactions |   #Train  |  #Test  | Density |
|:--------------:|:------:|:------:|:-------------:|:---------:|:-------:|:-------:|
| amazonbooks_x0 | 52,643 | 91,599 |   2,984,108   | 2,380,730 | 603,378 | 0.00062 |

Note that we fix **embedding_dim=64** following the setting in NGCF/LightGCN for fair comparisons.

|  Representation-based-Model |   Recall@20   |   Recall@50   |   NDCG@20   |   NDCG@50   |   HitRate@20   |   HitRate@50   | Steps-to-Reproduce | Contributed-by |
|----------------------------:|:-------------:|:-------------:|:-----------:|:-----------:|:--------------:|:--------------:|:------------------:|----------------|
|                 ItemPop |               |               |             |             |                |                |                    |                |
|                     ItemKNN |               |               |             |             |                |                |                    |                |
|                      MF-BPR |               |               |             |             |                |                |      notebook      |                |
|                      MF-CEL |               |               |             |             |                |                |                    |                |
|                        SLIM |               |               |             |             |                |                |                    |                |
|                     AutoRec |               |               |             |             |                |                |                    |                |
|                        MVAE |               |               |             |             |                |                |                    |                |
|                         CML |               |               |             |             |                |                |                    |                |
|                             |               |               |             |             |                |                |                    |                |
| **Interaction-based-Model** | **Recall@20** | **Recall@50** | **NDCG@20** | **NDCG@50** | **HitRate@20** | **HitRate@50** |                    |                |
|                       NeuMF |               |               |             |             |                |                |                    |                |


## Yelp

### yelp18_x0 (without side features)
We use this dataset following the same data splitting and preprocessing as in [NGCF](https://github.com/xiangwang1223/neural_graph_collaborative_filtering) and [LightGCN](https://github.com/kuandeng/LightGCN). We download the preprocessed data from [here](https://github.com/kuandeng/LightGCN/tree/master/Data/yelp2018). The data statistics are summarized as follows:

|                | #Users | #Items | #Interactions |   #Train  |  #Test  | Density |
|:--------------:|:------:|:------:|:-------------:|:---------:|:-------:|:-------:|
| amazonbooks_x0 | 31,668 | 38,048 |   1,561,406   | 1,237,259 | 324,147 | 0.00130 |

Note that we fix **embedding_dim=64** following the setting in NGCF/LightGCN for fair comparisons.

|  Representation-based-Model |   Recall@20   |   Recall@50   |   NDCG@20   |   NDCG@50   |   HitRate@20   |   HitRate@50   | Steps-to-Reproduce | Contributed-by |
|----------------------------:|:-------------:|:-------------:|:-----------:|:-----------:|:--------------:|:--------------:|:------------------:|----------------|
|                 ItemPop |               |               |             |             |                |                |                    |                |
|                     ItemKNN |               |               |             |             |                |                |                    |                |
|                      MF-BPR |               |               |             |             |                |                |      notebook      |                |
|                      MF-CEL |               |               |             |             |                |                |                    |                |
|                        SLIM |               |               |             |             |                |                |                    |                |
|                     AutoRec |               |               |             |             |                |                |                    |                |
|                        MVAE |               |               |             |             |                |                |                    |                |
|                         CML |               |               |             |             |                |                |                    |                |
|                             |               |               |             |             |                |                |                    |                |
| **Interaction-based-Model** | **Recall@20** | **Recall@50** | **NDCG@20** | **NDCG@50** | **HitRate@20** | **HitRate@50** |                    |                |
|                       NeuMF |               |               |             |             |                |                |                    |                |


