
# Open-CF-Benchmark

Towards Open Benchmarking for Collaborative Filtering

+ [Models](#models)
+ [Datasets](#datasets)
+ [Benchmarking results](./benchmarks/results.md) :+1: 


### Models
For our benchmarking, we have evaluated the following models with open-source code and reproducible steps.

| Publication |    Model   | Support MIPS? | Paper Title                                                                                      |
| ----:|:----------:|:-------------:|--------------------------------------------------------------------------------------------|
|  WWW'2001    |   ItemKNN  |       NO       |    Item-Based Collaborative Filtering Recommendation Algorithms                                                                                        |
| UAI'2009 |   MF-BPR   |      YES      | BPR: Bayesian Personalized Ranking from Implicit Feedback                         |
| ICDM'2011 |    SLIM    |      NO         | SLIM: Sparse Linear Methods for Top-N Recommender Systems                        |
| RecSys'2016 | YoutubeDNN |      YES      | Deep Neural Networks for YouTube Recommendations                               |
| WWW'2017 |    NeuMF   |       NO      | Neural Collaborative Filtering                                                    |
| WWW'2017 |     CML    |      YES      | Collaborative Metric Learning                                                     |
| SIGIR'2019 |    NGCF    |      YES      | Neural Graph Collaborative Filtering                                            |
| WWW'2019 |    EASE^R    |      NO      | Embarrassingly Shallow Autoencoders for Sparse Data                                         |
| AAAI'2020 |  LR-GCCF  |      YES      | Revisiting Graph based Collaborative Filtering: A Linear Residual Graph Convolutional Network Approach |
| SIGIR'2020 |  LightGCN  |      YES      | LightGCN: Simplifying and Powering Graph Convolution Network for Recommendation |
| TOIS'2020 |    ENMF    |      YES      | Efficient Neural Matrix Factorization without Sampling for Recommendation        |
| 2021 |   SimpleX   |      YES      |                                                                                            |


### Datasets
For our benchmarking, we employ the following open datasets that are commonly used in previous work.

| Dataset           | Dataset_ID           | Contain features? | Description                                                           |
|-------------------|----------------------|:-----------------:|-----------------------------------------------------------------------|
| AmazonBooks       | amazonbooks_x0       |         NO        | The preprocessed data is provided in [LightGCN](https://github.com/kuandeng/LightGCN/tree/master/Data/amazon-book).  |
|                   | amazonbooks_x1       |         YES        | The preprocessed data is provided in [ComiRec](https://github.com/THUDM/ComiRec).  |
| Yelp18            | yelp18_x0            |         NO        | The preprocessed data is provided in [LightGCN](https://github.com/kuandeng/LightGCN/tree/master/Data/yelp2018).  |
| Gowalla           | gowalla_x0           |         NO        | The preprocessed data is provided in [LightGCN](https://github.com/kuandeng/LightGCN/tree/master/Data/gowalla).  |
| Movielens1M       | movielens1m_x0       |         NO        | The preprocessed data is provided in [LCFN](https://github.com/Wenhui-Yu/LCFN/tree/master/dataset/Movielens).               |
|                   | movielens1m_x1       |         NO        | The preprocessed data is provided in NCF.                |
| Movielens10M      |                      |                   | TODO                                                                  |
| AmazonCDs       | amazoncds_x0        |         NO        | The preprocessed data is provided in BGCF.               |
| AmazonMovies       | amazonmovies_x0        |         NO        | The preprocessed data is provided in BGCF.               |
| AmazonBeauty       | amazonbeauty_x0        |         NO        | The preprocessed data is provided in BGCF.               |
| AmazonElectronics | amazonelectronics_x0 |         NO        | The preprocessed data is provided in [NBPO](https://github.com/Wenhui-Yu/NBPO/tree/master/dataset/amazon).               |
| CiteULike-A       | citeulikea_x0        |         NO        | The preprocessed data is provided in [DHCF](https://github.com/chenchongthu/ENMF#4-dhcf-kdd-2020dual-channel-hypergraph-collaborative-filtering).               |
| Taobao            | taobao_x0       |        YES        | The preprocessed data is provided in [ComiRec](https://github.com/THUDM/ComiRec).





