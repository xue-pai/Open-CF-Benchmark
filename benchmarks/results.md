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
|                 ItemPop     |     0.0051          |   0.0101            |    0.0044         |  0.0061           |     0.0419           |    0.0764            |    [link](https://github.com/xue-pai/Open-CF-Benchmarks/blob/master/benchmarks/ItemPop/ItemPop_amazonbooks_x0.md)                |       Kelong Mao         |
|                     ItemKNN |    0.0736           |  0.1175             |    0.0606         |   0.0771          |     0.3765           |     0.5234           |    [link](https://github.com/xue-pai/Open-CF-Benchmarks/blob/master/benchmarks/ItemKNN/ItemKNN_amazonbooks_x0.md)               |    Jinpeng Wang            |
|                      MF-BPR |               |               |             |             |                |                |      link      |                |
|                        SLIM [ICDM'20XX] |               |               |             |             |                |                |                    |                |
|                     AutoRec |              |               |             |             |                |                |                    |                |
|                        MVAE |               |               |             |             |                |                |                    |                |
|                         CML |               |               |             |             |                |                |                    |                |
|                         EASE^r [WWW'2019] |     0.0710          |   0.1177           |     0.0567        |   0.0744          |   0.3710            |      0.5293          |     [link](https://github.com/xue-pai/Open-CF-Benchmarks/blob/master/benchmarks/EASE_r/EASE_amazonbooks_x0.md)               |     XUEPAI           |
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
|                 ItemPop     |     0.0124          |   0.0242            |    0.0101         |      0.0145       |        0.0831        |     0.1493           |     [link](https://github.com/xue-pai/Open-CF-Benchmarks/blob/master/benchmarks/ItemPop/ItemPop_yelp18_x0.md)               |      Kelong Mao          |
|                     ItemKNN |   0.0639            |   0.1219            |    0.0531         |     0.0746        |      0.3876          |    0.5753            |     [link](https://github.com/xue-pai/Open-CF-Benchmarks/blob/master/benchmarks/ItemKNN/ItemKNN_yelp18_x0.md)               |      Jinpeng Wang          |
|                    MF-BPR |               |               |             |             |                |                |      link      |                |
|                        SLIM |               |               |             |             |                |                |                    |                |
|                     AutoRec |               |               |             |             |                |                |                    |                |
|                        MVAE |               |               |             |             |                |                |                    |                |
|                         CML |               |               |             |             |                |                |                    |                |
|                         EASE^r [WWW'2019] |     0.0657          |    0.1225           |     0.0552        |   0.0762          |      0.3966          |    0.5839            |    [link](https://github.com/xue-pai/Open-CF-Benchmarks/blob/master/benchmarks/EASE_r/EASE_yelp18_x0.md)                |    XUEPAI            |
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
|                 ItemPop     |    0.0416           |    0.0624           |     0.0317        |     0.0379        |       0.2038         |      0.2777          |     [link](https://github.com/xue-pai/Open-CF-Benchmarks/blob/master/benchmarks/ItemPop/ItemPop_gowalla_x0.md)               |     Kelong Mao           |
|                 ItemKNN |   0.1570           |   0.2549            |    0.1214         |     0.1527       |      0.5094         |    0.6650            |     [link](https://github.com/xue-pai/Open-CF-Benchmarks/blob/master/benchmarks/ItemKNN/ItemKNN_gowalla_x0.md)               |      Jinpeng Wang          |
|                  MF-BPR [UAI'2009] |               |               |             |             |                |                |      link      |                |
|                        SLIM |               |               |             |             |                |                |                    |                |
|                     AutoRec |               |               |             |             |                |                |                    |                |
|                        MVAE |               |               |             |             |                |                |                    |                |
|                         CML |               |               |             |             |                |                |                    |                |
|                         EASE^r [WWW'2019] |    0.1765           |    0.2701           |    0.1467         |     0.1760        |      0.5727          |      0.7081          |  [link](https://github.com/xue-pai/Open-CF-Benchmarks/blob/master/benchmarks/EASE_r/EASE_gowalla_x0.md)                  |     XUEPAI           |
|                      ENMF [TOIS'2020] |    0.1523        |  0.2379        |  0.1315     |     0.1583     |     0.5336      |   0.6701    |   [link](https://github.com/xue-pai/Open-CF-Benchmarks/blob/master/benchmarks/ENMF/ENMF_gowalla_x0.md)               |    Jinpeng Wang            |
|                             |               |               |             |             |                |                |                    |                |
| **Interaction-based-Model** | **Recall@20** | **Recall@50** | **NDCG@20** | **NDCG@50** | **HitRate@20** | **HitRate@50** |                    |                |
|                       NeuMF |               |               |             |             |                |                |                    |                |

