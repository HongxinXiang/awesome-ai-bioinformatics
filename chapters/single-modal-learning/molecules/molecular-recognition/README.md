# 1. Algorithm

## 1.1  Rule-based methods

| Name      | Programming language | Open-Source | Link                                                         |
| --------- | -------------------- | ----------- | ------------------------------------------------------------ |
| CliDE Pro | C++                  | No          | \[[Software](http://www.keymodule.co.uk/products/clide/clide-pro.html)] |
| ChemOCR   | Java                 | No          | [[Software](https://www.scai.fraunhofer.de/en/business-research-areas/bioinformatics/products/chemocr.html)] |
| OSRA      | C++                  | Yes         | [[Paper](https://pubs.acs.org/doi/10.1021/ci800067r)] \[[Code](https://github.com/metamolecular/osra)] \[[Web](https://cactus.nci.nih.gov/cgi-bin/osra/index.cgi)] [[Home](https://cactus.nci.nih.gov/osra/)] |
| Imago     | C++                  | Yes         | [[Paper](https://trec.nist.gov/pubs/trec20/papers/GGA.chemical.pdf)] [[Code](https://github.com/ctrltz/ocsr-project)] [[Home](https://lifescience.opensource.epam.com/imago/)] |
| MolVec    | Java                 | Yes         | [[Paper]()] [[Code](https://github.com/ncats/molvec)]        |



## 1.2 Deep learning-based methods

[**MSE-DUDL**] Molecular Structure Extraction from Documents Using Deep Learning (*J. Chem. Inf. Model.* 2019) [[Paper](https://pubs.acs.org/doi/10.1021/acs.jcim.8b00669)] 

![MSE_DUDL](https://pubs.acs.org/cms/10.1021/acs.jcim.8b00669/asset/images/medium/ci-2018-00669n_0002.gif)

---

[**Img2Mol**] Img2Mol - Accurate SMILES Recognition from Molecular Graphical Depictions (*Chem. Sci. 2021) [[Paper](https://pubs.rsc.org/en/content/articlehtml/2021/sc/d1sc01839f)] [[Code](https://github.com/bayer-science-for-a-better-life/Img2Mol)]

![Img2Mol](https://pubs.rsc.org/image/article/2021/SC/d1sc01839f/d1sc01839f-f3.gif)

----

[**ChemPix**] ChemPix: Automated Recognition of Hand-drawn Hydrocarbon Structures Using Deep Learning (*Chem. Sci.* 2021) [[Paper](https://chemrxiv.org/engage/chemrxiv/article-details/60c755d50f50dbb98f397fad)] [[Code](https://github.com/hayleyweir/im2smiles)]

![ChemPix](https://pubs.rsc.org/image/article/2021/SC/d1sc02957f/d1sc02957f-f1.gif)

---

[**ChemGrapher**] ChemGrapher: Optical Graph Recognition of Chemical Compounds by Deep Learning (*J. Chem. Inf. Model.* 2020)  [[Paper](https://pubs.acs.org/doi/10.1021/acs.jcim.0c00459)] [[Code](https://github.com/biolearning-stadius/chemgrapher-self-rich-labeling/)]

![ChemGrapher](https://pubs.acs.org/cms/10.1021/acs.jcim.0c00459/asset/images/medium/ci0c00459_0003.gif)

[**Oldenhof's model**] Self-labeling of Fully Mediating Representations by Graph Alignment (*BNAIC/Benelearn* 2021) [[Paper](https://link.springer.com/chapter/10.1007/978-3-030-93842-0_3)] [[Code](https://github.com/biolearning-stadius/chemgrapher-self-rich-labeling)]

![Graph Aligning](https://media.springernature.com/full/springer-static/image/chp%3A10.1007%2F978-3-030-93842-0_3/MediaObjects/521858_1_En_3_Fig1_HTML.png)

---

[**DECIMER**] DECIMER: towards deep learning for chemical image recognition (*J. Cheminform.* 2020) [[Paper](https://jcheminf.biomedcentral.com/articles/10.1186/s13321-020-00469-w)] [[Code](https://github.com/Kohulan/DECIMER-Image-to-SMILES)]

![DECIMER](https://media.springernature.com/lw685/springer-static/image/art%3A10.1186%2Fs13321-020-00469-w/MediaObjects/13321_2020_469_Fig3_HTML.png)

[**DECIMER 1.0**] DECIMER 1.0: Deep Learning for Chemical Image Recognition using Transformers (*J. Cheminform.* 2021) [[Paper](https://jcheminf.biomedcentral.com/articles/10.1186/s13321-021-00538-8)] [[Code](https://github.com/Kohulan/DECIMER-Image_Transformer)]

![DECIMER 1.0](https://media.springernature.com/lw685/springer-static/image/art%3A10.1186%2Fs13321-021-00538-8/MediaObjects/13321_2021_538_Fig3_HTML.png)

[**DECIMER-Segmentation**] DECIMER-Segmentation: Automated extraction of chemical structure depictions from scientific literature. (*J Cheminform* 2021) [[Paper](https://jcheminf.biomedcentral.com/articles/10.1186/s13321-021-00496-1)] [[Code](https://github.com/Kohulan/DECIMER-Image-Segmentation)]

![figure 2](https://media.springernature.com/lw685/springer-static/image/art%3A10.1186%2Fs13321-021-00496-1/MediaObjects/13321_2021_496_Fig2_HTML.png)

---

[**ABC-Net**] ABC-Net: a divide-and-conquer based deep learning architecture for SMILES recognition from molecular images (*Briefings in Bioinformatics* 2022) [[Paper]()] [[Code](https://github.com/zhang-xuan1314/ABC-Net)]

![ABC-Net](https://oup.silverchair-cdn.com/oup/backfile/Content_public/Journal/bib/23/2/10.1093_bib_bbac033/1/m_bbac033f1.jpeg?Expires=1666561016&Signature=i5qKarFKZJTBk9EvwygQFjx60e9WIbdKNw0UkMe~QORVI2yAAp~emdzF~eM5M2~uUb-3OZDINkwwZE0I1MLCtkBK8d~5~obxZtwvDsq~fY1yzlBsBYrWzlwU6czt~wlkRqzg~s5EvBGM1LnR6B2Ggb0-1svuH75XnkvPLkdw6ShxX7LDFjOfuGJfPvcZ~AU7Pt1MNSYdKhN0MjHA93-T3X2Q3ZIpjQ50T9ta53WKi-kgqC8tET6a~kHNA2Hp1AmpYdOPW~e7i7diBW27sravm8KyKoI3TG7FjFmJyWscj4xcM9w0FoFaxeynqp81wrgvOfAU-oJ9ur4P4vYnbXYM1A__&Key-Pair-Id=APKAIE5G5CRDK6RD3PGA)

[**MICER**] MICER: a pre-trained encoder–decoder architecture for molecular image captioning (*Bioinformatics* 2022) [[Paper](https://academic.oup.com/bioinformatics/advance-article-abstract/doi/10.1093/bioinformatics/btac545/6656348)] [[Code](https://github.com/Jiacai-Yi/MICER)]

![MICER](https://oup.silverchair-cdn.com/oup/backfile/Content_public/Journal/bioinformatics/PAP/10.1093_bioinformatics_btac545/2/m_btac545f2.jpeg?Expires=1666555956&Signature=rRrrZKsCmCTUG680uyimSJ74U2Iig~MRNE92X268hdTAIDEpSh76t9mDK5tN06ZhJ7WKTnfPWtECgv9Qc-F7I4OihDIakk9jmTCRDWVLllfC2IyWh-lhnyYIdUwLP6r8bHblIxNeWjc0PylL9KB9Amk1jD~wh9jUJZAWVzQ46lXGjaC9exqydvuIEBei4ucJhiw~o3LXhpTvp-h5lb6a~m3hBlyKw2JbtpvKrXhhKmyKW39g14akz9hG2atnyZ-RMIKXeeHFwQZ-96dyGW3uUhf5jKN61wrPegqvBdwX3eYfmvwzK7LZlHqSCX79dIO6rTAB8-KB7BgvcHIUlnyFwA__&Key-Pair-Id=APKAIE5G5CRDK6RD3PGA)

---

[**SwinOCSR**] SwinOCSR: end-to-end optical chemical structure recognition using a Swin Transformer (*J Cheminform* 2022) [[Paper](https://jcheminf.biomedcentral.com/articles/10.1186/s13321-022-00624-5)] [[Code](https://github.com/suanfaxiaohuo/SwinOCSR/tree/main)]

![SwinOCSR](https://media.springernature.com/lw685/springer-static/image/art%3A10.1186%2Fs13321-022-00624-5/MediaObjects/13321_2022_624_Fig2_HTML.png)

---

[**Qian's model**] Robust Molecular Image Recognition: A Graph Generation Approach (*arXiv* 2022) [[Paper](https://arxiv.org/abs/2205.14311)]

![Qian](./chapters/single-modal-learning/molecules/molecular-recognition/Qian.png)

---

[**MolMiner**] MolMiner: You only look once for chemical structure recognition (*J. Chem. Inf. Model.* 2022) [[Paper](https://pubs.acs.org/doi/10.1021/acs.jcim.2c00733)] [[Code](https://github.com/iipharma/pharmamind-molminer)]

![MolMiner](https://pubs.acs.org/cms/10.1021/acs.jcim.2c00733/asset/images/medium/ci2c00733_0005.gif)

---

[**Yoo's model**] Image-to-Graph Transformers for Chemical Structure Recognition (*ICASSP* 2022) [[Paper](https://ieeexplore.ieee.org/abstract/document/9746088)] 

![img2graph](https://ieeexplore.ieee.org/mediastore_new/IEEE/content/media/9745891/9746004/9746088/yoo1-p5-yoo-large.gif)

---

CEDe: A collection of expert-curated datasets with atom-level entity annotations for Optical Chemical Structure Recognition

# 2. Review

A review of optical chemical structure recognition tools (*J. Cheminform.* 2020) [[Paper](https://jcheminf.biomedcentral.com/articles/10.1186/s13321-020-00465-0)]
