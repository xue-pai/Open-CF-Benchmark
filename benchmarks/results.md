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
|                     ItemKNN [WWW'2001] |    0.0736           |  0.1175             |    0.0606         |   0.0771          |     0.3765           |     0.5234           |    [link](https://github.com/xue-pai/Open-CF-Benchmarks/blob/master/benchmarks/ItemKNN/ItemKNN_amazonbooks_x0.md)               |    Jinpeng Wang            |
|                      MF-BPR [UAI'2009] |    ~~0.0250~~           |        -       |     ~~0.0196~~        |     -        |        -        |          -      |      -     |    [Reported by NGCF paper](https://arxiv.org/abs/1905.08108)               |
|                                        |      0.0338         |     0.0660          |      0.0261       |    0.0380         |      0.2103          |       0.3530         |      link      |      XUEPAI          |
|                        SLIM [ICDM'2011] |    0.0755           |   0.1257            |   0.0602          |  0.0791           |     0.3873           |     0.5472           |   [link](https://github.com/xue-pai/Open-CF-Benchmarks/blob/master/benchmarks/SLIM/SLIM_amazonbooks_x0.md)                  |     Kelong Mao              |
|                     AutoRec |              |               |             |             |                |                |                    |                |
|                        MVAE |               |               |             |             |                |                |                    |                |
|                         CML [WWW'2017] |    0.0522           |   0.0953            |     0.0428        |    0.0591         |     0.2840           |     0.4410           |      [link](https://github.com/xue-pai/Open-CF-Benchmarks/blob/master/benchmarks/CML/CML_amazonbooks_x0.md)               |   Jinpeng Wang             |
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
|                     ItemKNN [WWW'2001]  |   0.0639            |   0.1219            |    0.0531         |     0.0746        |      0.3876          |    0.5753            |     [link](https://github.com/xue-pai/Open-CF-Benchmarks/blob/master/benchmarks/ItemKNN/ItemKNN_yelp18_x0.md)               |      Jinpeng Wang          |
|                    MF-BPR [UAI'2009] |      ~~0.0433~~         |      -         |   ~~0.0354~~          |       -         |         -          |      -             |       -      |     [Reported by NGCF paper](https://arxiv.org/abs/1905.08108)            |
|                                      |    0.0576           |      0.1123         |     0.0468        |   0.0671          |      0.3624          |       0.5577         |      link      |       XUEPAI         |
|                        SLIM [ICDM'2011] |    0.0646           |     0.1213          |    0.0541         |     0.0751        |    0.3912            |    0.5799            |     [link](https://github.com/xue-pai/Open-CF-Benchmarks/blob/master/benchmarks/SLIM/SLIM_yelp18_x0.md)                 |     Kelong Mao              |
|                     AutoRec |               |               |             |             |                |                |                    |                |
|                        MVAE |               |               |             |             |                |                |                    |                |
|                         CML [WWW'2017] |     0.0622          |   0.1181            |   0.0536          |   0.0738          |      0.3810          |     0.5510           |     [link](https://github.com/xue-pai/Open-CF-Benchmarks/blob/master/benchmarks/CML/CML_yelp18_x0.md)                |     Jinpeng Wang               |
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
| gowalla_x0 | 29,858  | 40,981  |  1,027,370    | 810,128  | 217,242  |  0.00084  |

Note that we fix **embedding_dim=64** following the setting in NGCF/LightGCN for fair comparisons.

|  Representation-based-Model |   Recall@20   |   Recall@50   |   NDCG@20   |   NDCG@50   |   HitRate@20   |   HitRate@50   | Steps-to-Reproduce | Contributed-by |
|----------------------------:|:-------------:|:-------------:|:-----------:|:-----------:|:--------------:|:--------------:|:------------------:|----------------|
|                 ItemPop     |    0.0416           |    0.0624           |     0.0317        |     0.0379        |       0.2038         |      0.2777          |     [link](https://github.com/xue-pai/Open-CF-Benchmarks/blob/master/benchmarks/ItemPop/ItemPop_gowalla_x0.md)               |     Kelong Mao           |
|                 ItemKNN [WWW'2001]  |   0.1570           |   0.2549            |    0.1214         |     0.1527       |      0.5094         |    0.6650            |     [link](https://github.com/xue-pai/Open-CF-Benchmarks/blob/master/benchmarks/ItemKNN/ItemKNN_gowalla_x0.md)               |      Jinpeng Wang          |
|                  MF-BPR [UAI'2009] |   ~~0.1291~~         |       -        |     ~~0.1109~~        |    -           |     -             |       -           |      -        |          [Reported by NGCF paper](https://arxiv.org/abs/1905.08108)   |
|                                    |   0.1627            |    0.2533           |    0.1378         |   0.1662          |        0.5544        |    0.6936            |      link      |       XUEPAI         |
|                        SLIM [ICDM'2011] |    0.1699           |    0.2658           |    0.1382         |     0.1687        |       0.5564         |    0.6960            |   [link](https://github.com/xue-pai/Open-CF-Benchmarks/blob/master/benchmarks/SLIM/SLIM_gowalla_x0.md)                  |     Kelong Mao            |
|                     AutoRec |               |               |             |             |                |                |                    |                |
|                        MVAE |               |               |             |             |                |                |                    |                |
|                         CML [WWW'2017] |   0.1670            |   0.2602            |   0.1292          |     0.1587        |      0.5410          |        0.6750        |   [link](https://github.com/xue-pai/Open-CF-Benchmarks/blob/master/benchmarks/CML/CML_gowalla_x0.md)                  |     Jinpeng Wang              |
|                         EASE^r [WWW'2019] |    0.1765           |    0.2701           |    0.1467         |     0.1760        |      0.5727          |      0.7081          |  [link](https://github.com/xue-pai/Open-CF-Benchmarks/blob/master/benchmarks/EASE_r/EASE_gowalla_x0.md)                  |     XUEPAI           |
|                      ENMF [TOIS'2020] |    0.1523        |  0.2379        |  0.1315     |     0.1583     |     0.5336      |   0.6701    |   [link](https://github.com/xue-pai/Open-CF-Benchmarks/blob/master/benchmarks/ENMF/ENMF_gowalla_x0.md)               |    Jinpeng Wang            |
|                             |               |               |             |             |                |                |                    |                |
| **Interaction-based-Model** | **Recall@20** | **Recall@50** | **NDCG@20** | **NDCG@50** | **HitRate@20** | **HitRate@50** |                    |                |
|                       NeuMF |               |               |             |             |                |                |                    |                |

