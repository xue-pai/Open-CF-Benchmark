# Benchmarking Results

Indexed by datasets
+ [AmazonBooks](#amazonbooks)
+ [Yelp18](#Yelp18)
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
|                 ItemPop     |               |               |             |             |                |                |                    |                |
|                     ItemKNN |    0.0736           |  0.1175             |    0.0606         |   0.0771          |     0.3765           |     0.5234           |    [link](https://github.com/xue-pai/Open-CF-Benchmarks/blob/master/benchmarks/ItemKNN/ItemKNN_amazonbooks_x0.md)               |    Jinpeng Wang            |
|                      MF-BPR |               |               |             |             |                |                |      link      |                |
|                        SLIM |               |               |             |             |                |                |                    |                |
|                     AutoRec |               |               |             |             |                |                |                    |                |
|                        MVAE |               |               |             |             |                |                |                    |                |
|                         CML |               |               |             |             |                |                |                    |                |
|                         EASE^r [WWW'2019] |     0.070962          |   0.117733            |     0.056734        |   0.074354          |   0.371008             |      0.529282          |     [link](https://github.com/xue-pai/Open-CF-Benchmarks/blob/master/benchmarks/EASE_r/EASE_amazonbooks_x0.md)               |     XUEPAI           |
|                         ENMF [TOIS'2020] |    0.0359           |   0.0691           |  0.0281           |      0.0404       |      0.2187          |    0.3649            |   [link](https://github.com/xue-pai/Open-CF-Benchmarks/blob/master/benchmarks/ENMF/ENMF_amazonbooks_x0.md)               |    Jinpeng Wang            |
|                             |               |               |             |             |                |                |                    |                |
| **Interaction-based-Model** | **Recall@20** | **Recall@50** | **NDCG@20** | **NDCG@50** | **HitRate@20** | **HitRate@50** |                    |                |
|                       NeuMF |               |               |             |             |                |                |                    |                |


## Yelp18

### yelp18_x0 (without side features)
We use this dataset following the same data splitting and preprocessing as in [NGCF](https://github.com/xiangwang1223/neural_graph_collaborative_filtering) and [LightGCN](https://github.com/kuandeng/LightGCN). We download the preprocessed data from [here](https://github.com/kuandeng/LightGCN/tree/master/Data). The data statistics are summarized as follows:

|                | #Users | #Items | #Interactions |   #Train  |  #Test  | Density |
|:--------------:|:------:|:------:|:-------------:|:---------:|:-------:|:-------:|
| amazonbooks_x0 | 31,668 | 38,048 |   1,561,406   | 1,237,259 | 324,147 | 0.00130 |

Note that we fix **embedding_dim=64** following the setting in NGCF/LightGCN for fair comparisons.

|  Representation-based-Model |   Recall@20   |   Recall@50   |   NDCG@20   |   NDCG@50   |   HitRate@20   |   HitRate@50   | Steps-to-Reproduce | Contributed-by |
|----------------------------:|:-------------:|:-------------:|:-----------:|:-----------:|:--------------:|:--------------:|:------------------:|----------------|
|                 ItemPop     |               |               |             |             |                |                |                    |                |
|                     ItemKNN |   0.0639            |   0.1219            |    0.0531         |     0.0746        |      0.3876          |    0.5753            |     [link](https://github.com/xue-pai/Open-CF-Benchmarks/blob/master/benchmarks/ItemKNN/ItemKNN_yelp18_x0.md)               |      Jinpeng Wang          |
|                    MF-BPR |               |               |             |             |                |                |      link      |                |
|                        SLIM |               |               |             |             |                |                |                    |                |
|                     AutoRec |               |               |             |             |                |                |                    |                |
|                        MVAE |               |               |             |             |                |                |                    |                |
|                         CML |               |               |             |             |                |                |                    |                |
|                         EASE^r [WWW'2019] |     0.065707          |    0.122483           |     0.055216        |   0.076210          |      0.396615          |    0.583902            |    [link](https://github.com/xue-pai/Open-CF-Benchmarks/blob/master/benchmarks/EASE_r/EASE_yelp18_x0.md)                |    XUEPAI            |
|                      ENMF [TOIS'2020] |    0.0624          |  0.1189         |  0.0515       |     0.0723      |      0.3848         |    0.5792       |   [link](https://github.com/xue-pai/Open-CF-Benchmarks/blob/master/benchmarks/ENMF/ENMF_yelp18_x0.md)               |    Jinpeng Wang            |
|                             |               |               |             |             |                |                |                    |                |
| **Interaction-based-Model** | **Recall@20** | **Recall@50** | **NDCG@20** | **NDCG@50** | **HitRate@20** | **HitRate@50** |                    |                |
|                       NeuMF |               |               |             |             |                |                |                    |                |


## Gowalla

### gowalla_x0 (without side features)
We use this dataset following the same data splitting and preprocessing as in [NGCF](https://github.com/xiangwang1223/neural_graph_collaborative_filtering) and [LightGCN](https://github.com/kuandeng/LightGCN). We download the preprocessed data from [here](https://github.com/kuandeng/LightGCN/tree/master/Data). The data statistics are summarized as follows:

|                | #Users | #Items | #Interactions |   #Train  |  #Test  | Density |
|:--------------:|:------:|:------:|:-------------:|:---------:|:-------:|:-------:|
| gowalla_x0 |   |   |      |   |   |   |

Note that we fix **embedding_dim=64** following the setting in NGCF/LightGCN for fair comparisons.

|  Representation-based-Model |   Recall@20   |   Recall@50   |   NDCG@20   |   NDCG@50   |   HitRate@20   |   HitRate@50   | Steps-to-Reproduce | Contributed-by |
|----------------------------:|:-------------:|:-------------:|:-----------:|:-----------:|:--------------:|:--------------:|:------------------:|----------------|
|                 ItemPop     |               |               |             |             |                |                |                    |                |
|                  ItemKNN |   0.1570           |   0.2549            |    0.1214         |     0.1527       |      0.5094         |    0.6650            |     [link](https://github.com/xue-pai/Open-CF-Benchmarks/blob/master/benchmarks/ItemKNN/ItemKNN_gowalla_x0.md)               |      Jinpeng Wang          |
|                  MF-BPR |               |               |             |             |                |                |      link      |                |
|                        SLIM |               |               |             |             |                |                |                    |                |
|                     AutoRec |               |               |             |             |                |                |                    |                |
|                        MVAE |               |               |             |             |                |                |                    |                |
|                         CML |               |               |             |             |                |                |                    |                |
|                         EASE^r [WWW'2019] |    0.176493           |    0.270126           |    0.146657         |     0.175974        |      0.572677          |      0.708051          |  [link](https://github.com/xue-pai/Open-CF-Benchmarks/blob/master/benchmarks/EASE_r/EASE_gowalla_x0.md)                  |     XUEPAI           |
|                      ENMF [TOIS'2020] |    0.1523        |  0.2379        |  0.1315     |     0.1583     |     0.5336      |   0.6701    |   [link](https://github.com/xue-pai/Open-CF-Benchmarks/blob/master/benchmarks/ENMF/ENMF_gowalla_x0.md)               |    Jinpeng Wang            |
|                             |               |               |             |             |                |                |                    |                |
| **Interaction-based-Model** | **Recall@20** | **Recall@50** | **NDCG@20** | **NDCG@50** | **HitRate@20** | **HitRate@50** |                    |                |
|                       NeuMF |               |               |             |             |                |                |                    |                |

