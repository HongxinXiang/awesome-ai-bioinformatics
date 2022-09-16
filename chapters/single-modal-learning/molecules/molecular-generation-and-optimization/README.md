
# 1. Datasets

* [ZINC](http://zinc15.docking.org/): 736M Compounds.
* [ChEMBL](https://www.ebi.ac.uk/chembl/): 23M Compounds, 197M Activities.
* [QM9](http://quantum-machine.org/datasets/):
* [PubChem](https://pubchem.ncbi.nlm.nih.gov/): 112M Compounds, 296M Bioactivities.


# 2. Algorithm

## 2.1 Molecular generation Methods

### 2.1.1 VAE-based
+ SMILES

[**GVAE**] Grammar variational autoencoder.(ICML 2017)\[[Paper](https://arxiv.org/pdf/1703.01925.pdf)] \[[Code](https://github.com/mkusner/grammarVAE)\]

[**chemical VAE**] Automatic chemical design using a data-driven continuous representation of molecules (ACS Cent. Sci. 2018)\[[Paper](https://pubs.acs.org/doi/pdf/10.1021/acscentsci.7b00572)] \[[Code](https://github.com/aspuru-guzik-group/chemical_vae)\]

[**SD-VAE**] Syntax-directed variational autoencoder for molecule generation (ICLR 2018)\[[Paper](https://hanjun-dai.github.io/pdf/sdvae_workshop_camera_ready.pdf)] \[[Code](https://github.com/Hanjun-Dai/sdvae)\]

+ Graph

[**JT-VAE**] Junction tree variational autoencoder for molecular graph generation (ICML 2018) \[[Paper](https://arxiv.org/pdf/1802.04364.pdf)] \[[Code](https://github.com/wengong-jin/icml18-jtnn)\]

[**GraphVAE**] Graphvae: Towards generation of small graphs using variational autoencoders.(ICANN 2018) \[[Paper](https://link.springer.com/chapter/10.1007/978-3-030-01418-6_41)]

[**CGVAE**] Constrained graph variational autoencoders for molecule design (NeurIPS 2018) \[[Paper](https://proceedings.neurips.cc/paper/2018/file/b8a03c5c15fcfa8dae0b03351eb1742f-Paper.pdf)] \[[Code](https://github.com/Microsoft/constrained-graph-variational-autoencoder)\]

[**RationaleRL**] Multi-objective molecule generation using interpretable substructures (ICML 2020) \[[Paper](http://proceedings.mlr.press/v119/jin20b/jin20b.pdf)] \[[Code](https://github.com/wengong-jin/multiobj-rationale)\]

[**NEVAE**] NEVAE: A deep generative model for molecular graphs (AAAI 2020) \[[Paper](https://ojs.aaai.org//index.php/AAAI/article/view/3903)] \[[Code](https://github.com/Networks-Learning/nevae)\]


### 2.1.2 RNN-based
+ SMILES

[**Segler's model**] Generating focused molecule libraries for drug discovery with recurrent neural networks (ACS Cent. Sci. 2018)\[[Paper](https://pubs.acs.org/doi/pdf/10.1021/acscentsci.7b00512)]

[**CLM**] Generative molecular design in low data regimes. (Nat. Mach. Intell. 2020)\[[Paper](https://www.nature.com/articles/s42256-020-0160-y)] \[[Code](https://github.com/ETHmodlab/virtual_libraries)\]

[**DDC**] Direct steering of de novo molecular generation with descriptor conditional recurrent neural networks. (Nat. Mach. Intell. 2020)\[[Paper](https://www.nature.com/articles/s42256-020-0174-5)] \[[Code](https://github.com/pcko1/Deep-Drug-Coder)\]

[**BIMODAL**] Bidirectional molecule generation with recurrent neural networks. (J. Chem. Inf. Model. 2020)\[[Paper](https://pubs.acs.org/doi/pdf/10.1021/acs.jcim.9b00943)] \[[Code](https://github.com/ETHmodlab/BIMODAL)\]

[**Scaffold Decorator**] SMILES-based deep generative scaffold decorator for de-novo drug design. (J. Cheminform 2020)\[[Paper](https://jcheminf.biomedcentral.com/articles/10.1186/s13321-020-00441-8)] \[[Code](https://github.com/undeadpixel/reinvent-scaffold-decorator)\]

+ Graph

[**Li's model**] Learning deep generative models of graphs (ICLR 2018) \[[Paper](https://arxiv.org/pdf/1803.03324.pdf)]

[**Li's model**] Multi-objective de novo drug design with conditional graph generative model (J. Cheminform. 2018) \[[Paper](https://link.springer.com/content/pdf/10.1186/s13321-018-0287-6.pdf)] \[[Code](https://github.com/kevinid/molecule_generator)\]

[**MolecularRNN**] MolecularRNN: Generating realistic molecular graphs with optimized properties (arXiv 2019) \[[Paper](https://arxiv.org/pdf/1905.13372.pdf)]


### 2.1.3 GAN-based
+ SMILES

[**ORGAN**] Objective-reinforced generative adversarial networks (ORGAN) for sequence generation models (arXiv 2017)\[[Paper](https://arxiv.org/pdf/1705.10843.pdf)] \[[Code](https://github.com/gablg1/ORGAN)\]

[**ORGANIC**] Optimizing distributions over molecular space. An objective reinforced generative adversarial network for inverse-design chemistry (ORGANIC) (ChemRxiv 2017)\[[Paper](https://chemrxiv.org/engage/api-gateway/chemrxiv/assets/orp/resource/item/60c73d91702a9beea7189bc2/original/optimizing-distributions-over-molecular-space-an-objective-reinforced-generative-adversarial-network-for-inverse-design-chemistry-organic.pdf)] \[[Code](https://github.com/aspuru-guzik-group/ORGANIC)\]

[**latentGAN**] A de novo molecular generation method using latent vector based generative adversarial network. (J. Cheminform. 2019)\[[Paper](https://jcheminf.biomedcentral.com/articles/10.1186/s13321-019-0397-9)] \[[Code](https://github.com/Dierme/latent-gan)\]

[**stacked GAN**] De novo generation of hit-like molecules from gene expression signatures using artificial intelligence. (Nat. Commun. 2020)\[[Paper](https://www.nature.com/articles/s41467-019-13807-w)]

+ Graph

[**MolGAN**] MolGAN: An implicit generative model for smallmolecular graphs (ICML workshop 2018) \[[Paper](https://arxiv.org/pdf/1805.11973.pdf)] \[[Code](https://github.com/nicola-decao/MolGAN)\]

[**Mol-CycleGAN**] Mol-CycleGAN: a generative model for molecular optimization (J. Cheminform. 2020) \[[Paper](https://jcheminf.biomedcentral.com/articles/10.1186/s13321-019-0404-1)] \[[Code](https://github.com/ardigen/mol-cycle-gan)\]


### 2.1.4 Flow-based
[**GraphNVP**] GraphNVP: An invertible flow model for generating molecular graphs (arXiv 2019) \[[Paper](https://arxiv.org/pdf/1905.11600.pdf)] \[[Code](https://github.com/pfnet-research/graph-nvp)\]

[**GRF**] Graph residual flow for molecular graph generation (arXiv 2019) \[[Paper](https://arxiv.org/pdf/1909.13521.pdf)]

[**GraphAF**] GraphAF: a flow-based autoregressive model for molecular graph generation (ICLR 2020) \[[Paper](https://arxiv.org/abs/2001.09382)] \[[Code](https://drive.google.com/drive/folders/1FmYWcT8jDrwZlzPbmMpRhulb9OKTDWJL)\]

[**MoFlow**] MoFlow: an invertible flow model for generating molecular graphs (KDD 2020) \[[Paper](https://arxiv.org/pdf/2006.10137.pdf)] \[[Code](https://github.com/calvin-zcx/moflow)\]

[**MolGrow**] MolGrow: A graph normalizing flow for hierarchical molecular generation (AAAI 2021) \[[Paper](https://www.aaai.org/AAAI21Papers/AAAI-3802.KuznetsovM.pdf)]


## 2.2 Molecular optimization Methods


# 3. Metrics

# 4. Target properities
+ c-Jun N-terminal kinase 3 (JNK3)
+ glycogen synthase kinase 3β (GSK-3β)
+ quantitative estimate of drug-likeness (QED)
+ synthetic accessibility (SA)

# 5. Strategies
valency-based rejection sampling: ensure molecular validility