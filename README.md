# Open-CF-benchmarks


### Datasets
In our benchmarks, we employ the following open datasets that are commonly used in existing work.

| Dataset           | Dataset_ID           | Contain features? | Description                                                           |
|-------------------|----------------------|:-----------------:|-----------------------------------------------------------------------|
| AmazonBooks       | amazonbooks_x0       |         NO        | Following the data splitting and preprocessing in NGCF and LightGCN.  |
| Yelp18            | yelp18_x0            |         NO        | Following the data splitting and preprocessing in NGCF and LightGCN.  |
| Gowalla           | gowalla_x0           |         NO        | Following the data splitting and preprocessing in NGCF and LightGCN.  |
| Movielens1M       | movielens1m_x0       |         NO        | Following the data splitting and preprocessing in LCFN.               |
|                   | movielens1m_x1       |         NO        | Following the data splitting and preprocessing in NCF.                |
| Movielens10M      |                      |                   | TODO                                                                  |
| CiteULike-A       | citeulikea_x0        |         NO        | Following the data splitting and preprocessing in DHCF.               |
| AmazonElectronics | amazonelectronics_x0 |         NO        | Following the data splitting and preprocessing in NBPO.               |
| Frappe            |                      |        YES        | TODO                                                                  |
| Taobao            |                      |        YES        | TODO                                                                  |


### Models
In our benchmarks, we have evaluated the following models with open-source code and reproducible steps.

| Year |    Model   | Support MIPS? | Paper                                                                                      |
|:----:|:----------:|:-------------:|--------------------------------------------------------------------------------------------|
|   -  |   ItemPop  |       -       |                                                                                            |
|      |   ItemKNN  |       -       |                                                                                            |
| 2009 |   MF-BPR   |      YES      | [UAI'09] BPR: Bayesian Personalized Ranking from Implicit Feedback                         |
| 2009 |     ALS    |      YES      | [Computer'09] Matrix Factorization Techniques for Recommender Systems                      |
| 2011 |    SLIM    |               | [ICDM'11] SLIM: Sparse Linear Methods for Top-N Recommender Systems                        |
| 2016 | YouTubeNet |      YES      | [RecSys'16] Deep Neural Networks for YouTube Recommendations                               |
| 2017 |     GMF    |      YES      | [WWW'17] Neural Collaborative Filtering                                                    |
| 2017 |    NeuMF   |       NO      | [WWW'17] Neural Collaborative Filtering                                                    |
| 2017 |     CML    |      YES      | [WWW'17] Collaborative Metric Learning                                                     |
| 2019 |    NGCF    |      YES      | [SIGIR'19] Neural Graph Collaborative Filtering                                            |
| 2020 |  LightGCN  |      YES      | [SIGIR'20] LightGCN: Simplifying and Powering Graph Convolution Network for Recommendation |
| 2020 |    ENMF    |      YES      | [TOIS'20] Efficient Neural Matrix Factorization without Sampling for Recommendation        |
| 2020 |   MF-CEL   |      YES      |                                                                                            |



