# Missense variant effect predictions

Variant effect predictions produced by the [Ensembl Variant Effect Predictor](https://www.ensembl.org/info/docs/tools/vep/index.html) for genes in the [Ensembl 97](https://www.ensembl.org/index.html) release. Variants are collapsed, meaning that they are only shown once for every gene. File names indicate the chromosomes.

Every file contains a tab-delimited table with the following columns:

- **Gene**: The Ensembl gene identifier
- **Uploaded_variation**: The variant identifier
- **Location**: the 1-based location of the variant
- **codon_position**: position in the codon
- **ref**: reference 3-mer (the affected amino acid is typically in the middle)
- **alt**: the alternative 3-mer
- **cosine_similarity**: cosine similarity between the reference and the alternatie 3-mer (see [here](https://github.com/ehsanasgari/Deep-Proteomics))
- **pos_standardized**: starting position of the affected codon
- **polyphen_score**: Average PolyPhen-2 score across transcripts
- **sift_score**: Average SIFT score across transcripts
- **n** the number of affected transcripts
- **impact** (_polyphen\_score_ + (1 - _sift\_score_))/2


References:

```
@article{mclaren2016ensembl,
  title={The ensembl variant effect predictor},
  author={McLaren, William and Gil, Laurent and Hunt, Sarah E and Riat, Harpreet Singh and Ritchie, Graham RS and Thormann, Anja and Flicek, Paul and Cunningham, Fiona},
  journal={Genome biology},
  volume={17},
  number={1},
  pages={1--14},
  year={2016},
  publisher={BioMed Central}
}

@article{ng2003sift,
  title={SIFT: Predicting amino acid changes that affect protein function},
  author={Ng, Pauline C and Henikoff, Steven},
  journal={Nucleic acids research},
  volume={31},
  number={13},
  pages={3812--3814},
  year={2003},
  publisher={Oxford University Press}
}

@article{adzhubei2013predicting,
  title={Predicting functional effect of human missense mutations using PolyPhen-2},
  author={Adzhubei, Ivan and Jordan, Daniel M and Sunyaev, Shamil R},
  journal={Current protocols in human genetics},
  volume={76},
  number={1},
  pages={7--20},
  year={2013},
  publisher={Wiley Online Library}
}

@article{asgari2015continuous,
  title={Continuous Distributed Representation of Biological Sequences for Deep Proteomics and Genomics},
  author={Asgari, Ehsaneddin and Mofrad, Mohammad RK},
  journal={PloS one},
  volume={10},
  number={11},
  pages={e0141287},
  year={2015},
  publisher={Public Library of Science}
}

```
