# Benchmarking Results

Indexed by datasets
+ [AmazonBooks](#amazonbooks)
+ Yelp18
+ Gowalla
+ Movielens1M
+ Movielens10M
+ AmazonElectronics

## AmazonBooks

### amazonbooks_x0 (without side features)
This dataset follows the same data splitting and preprocessing as in [NGCF](https://github.com/xiangwang1223/neural_graph_collaborative_filtering) and [LightGCN](https://github.com/kuandeng/LightGCN). We download the preprocessed data from [here](https://github.com/kuandeng/LightGCN/tree/master/Data/amazon-book). The data statistics and the corresponding benchmarking results as follows:

|                | #Users | #Items | #Interactions |   #Train  |  #Test  | Density |
|:--------------:|:------:|:------:|:-------------:|:---------:|:-------:|:-------:|
| amazonbooks_x0 | 52,643 | 91,599 |   2,984,108   | 2,380,730 | 603,378 | 0.00062 |

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

