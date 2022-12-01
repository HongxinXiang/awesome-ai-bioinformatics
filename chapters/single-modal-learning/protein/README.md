# 1. Protein-related task
- protein function prediction
  - Enzyme reaction
  - GO term
  - EC (Enzyme Commission) number
- protein fold classification
- structural similarity prediction
- protein-ligand binding affinity prediction


# 2. Benchmark datasets

## 2.1 Protein function prediction

### Enzyme reaction (React.)

**Dataset.** This data set contains **37,428 proteins from 384 different EC numbers** ([baike](https://baike.baidu.com/item/EC%E7%BC%96%E5%8F%B7/9728081?fromModule=search-result_lemma), [wiki](https://en.wikipedia.org/wiki/Enzyme_Commission_number)) . The task consists of, given a 3D structure of an enzyme, to predict its complete EC number, e.g. 4.2.3.1, among the 384 numbers available in the dataset. The proteins in the data set are split into three sets, training, validation, and testing, whereby proteins in each set do not have more than 50% of sequence similarity with proteins from the other sets. Thus, we obtain 29,215 proteins for training, 2,562 proteins for validation, and 5,651 for testing.

**Metric.** Performance is measured with **mean accuracy** on the test set.



### GO term

**Dataset.** This dataset contains **36,641 proteins annotated with different Gene Ontology (GO) terms**. Proteins are selected to obtain between 50 and 5,000 proteins annotated for each individual GO term during training. The GO is organized hierarchically, and the data set considers three different sub-branches on the hierarchy: Molecular Function (MF), Biological Process (BP), and Cellular Component (CC) terms. Each sub-branch is predicted separately, using a different model to predict each term type separately. The number of GO terms for each sub-branch is 489 terms for the MF sub-branch, 1,943 terms for the BP sub-branch, and 320 terms for the CC sub-branch. The data set is organized in training, validation, and test sets, each containing 29,902, 3,323, and 3,416 proteins. The proteins in the test set contain only experimentally determined functions and are classified based on their sequence similarity to the train set, having < 30 %, < 40 %, < 50 %, < 70 %, or < 95 % similarity. Results are reported on the complete test set. However, this classification allow us to evaluate the generalization ability of our pre-trained models for different sequence similarity levels.

**Metric.** Performance is measured **using protein-centric maximum F-Score**, $F_{max}$. This metric measures the precision and recall of the predictions for each protein independently, and computes their mean. These means are then used to compute the F-score. $F_{max}$ is the maximum F-score among the different thresholds t tested in the range [0,1]. Formally:

$F_{max}=\mathop{max}\limits_{t}\{\frac{2p(t)r(t)}{p(t)+r(t)}\}$ , $p(t)=\frac{1}{|M(t)|}\sum_{i\in M(t)}\frac{|TP_i(t)|}{|Pred_i(t)|}$, $r(t)=\frac{1}{|N|}\sum_{i\in N}\frac{|TP_i(t)|}{|P_i|}$

where $TP_i(t)$ if the set of correctly predicted GO terms for protein i using threshold t, $Pred_i(t)$ if the set of predicted GO terms for protein $i$ using threshold $t$, $N$ is the set of all proteins in the test set, and $M(t)$ is the set of proteins for which we predict at least one GO term using threshold $t$.



### EC number

**Dataset.** the EC numbers contains 19,198 proteins (15,550 train set, 1,729 validation set and 1,919 test set), which are selected from the third and fourth levels of the EC tree, forming 538 binary classification tasks. **The EC numbers describe protein catalysis of biochemical reactions**. Both EC and GO prediction aim to answer the question: whether a protein has a particular function. This task is essentially the same as Enzyme reaction prediction.

**Metric.** As same as GO term prediction, the performance is measured **using protein-centric maximum F-Score**, $F_{max}$. 



## 2.2 Protein fold classification

### Fold

**Dataset.** This dataset contains **16,712 proteins domains of 1,195 different folds from the SCOPe 1.75 database**. The dataset provides a train, validation, and three different test sets with increasing difficulty based on the similarity between the proteins in the train and test sets: **Protein, Family, and Superfamily**. The train set is composed of 12,312 proteins whilst the validation set contains 736 proteins. The **Superfamily test set** contains 718 proteins belonging to different superfamilies as the proteins in the train set, the **Family test set** contains 1,254 proteins belonging to different families as the proteins in the train set, and the **Protein test set** contains 1,272 from the same families as the proteins in the train set.

**Metric.** Performance is measured with **mean accuracy** on the test sets.




## 2.3 Structural similarity prediction
### DaliLite

**Dataset.** This data set is composed of **140 protein domains from the SCOPe database for which similar proteins have to be found from a set of 15,211 protein chains**. Moreover, they provide another set composed of 176,022 protein chains, which can be use to train distance metric. In this benchmark, **different similarity levels are considered** based on the SCOPe classification hierarchy, Fold, Superfamily, and Family.

**Metric.** $F_{max}=\mathop{max}\limits_{n}\frac{2p(n)r(n)}{p(n)+r(n)}=\mathop{max}\limits_{n}\frac{2TP(n)}{n+T}$ ($p(n)$ is precision, $r(n)$ is recall, $T$ is the number of structures in the class)



### GraSR 

**Dataset.** This dataset contains two sets, **13,265 protein domains from the SCOPe database used as queries for comparison and 1,914 protein chains from the PDB database used as targets.**

**Metric.** This dataset considers a hit when the TMScore between the target protein chain and the protein domain is higher than $0.9\times m$, where $m$ is the maximum TMScore between the target protein and all the query protein domains in the main set.The performance is measured with **the hit ratio of the first $k$ query proteins** in the sorted list: $HR_k=\frac{1}{T}\sum_{i=1}^T\frac{N'_i(k)}{min(k,N_i)}$



## 2.4 Protein-ligand binding affinity prediction

**Dataset.** This dataset contains **4,709 filtered pairs of protein-ligand from the PDBind database (version 2019)** with their corresponding binding affinity, expressed in molar units of the inhibition constant (Ki) or dissociation constant (Kd). We do not distinguish between these constants and predict the negative log transformation of these, pK = −log(K). This task contains two different datasets with different maximum sequence similarity between the train and test set, 60% and 30%. Each of these is further divided into train, validation, and test sets, each containing 3,507, 466, and 490 respectively for the 30 % dataset, and 3,678, 460, and 460 for the 60 % dataset.

**Metric.** Performance is measured with **root mean squared error (RMSE)**, and Pearson and Spearman correlation coefficients.



# References

Zhang, Zuobai, et al. "Protein representation learning by geometric structure pretraining." *arXiv preprint arXiv:2203.06125* (2022).

Hermosilla, Pedro, and Timo Ropinski. "Contrastive representation learning for 3d protein structures." arXiv preprint arXiv:2205.15675 (2022).
