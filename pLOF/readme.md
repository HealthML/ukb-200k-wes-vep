# Protein loss of function variant effect predictions

Variant effect predictions produced by the [Ensembl Variant Effect Predictor](https://www.ensembl.org/info/docs/tools/vep/index.html) for genes in the [Ensembl 97](https://www.ensembl.org/index.html) release. Variants are collapsed, meaning that they are only shown once for every gene. File names indicate the chromosomes.

All variants marked as splice\_acceptor\_variant, splice\_donor\_variant, frameshift\_variant, stop\_gained, stop\_lost or start\_lost were considered protein loss of function (pLOF).

Each file contains a tab-separated table with the follwing columns:
- **Uploaded_variation**: variant identifier
- **Location**: 1-based variant position
- **Allele**: alternative allele
- **Gene**: Ensembl gene identifier
- **n_affected**: number of transcripts affected

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

```
