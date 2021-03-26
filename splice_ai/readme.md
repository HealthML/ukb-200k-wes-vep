# Splice variant effect predictions

Variant effect predictions produced by [SpliceAI](https://github.com/Illumina/SpliceAI). There are the masked splice-site-proximal delta scores (1.3) intersected with UK Biobank variants and filtered to keep only variants with at least one delta score >= 0.1. Only performed for single nucleotide variants (SNVs).


Every file contains a tab-delimited table with the following columns:

- **name**: The variant identifier
- **chrom**: chromosome
- **start**: the 0-based start position of the variant
- **end**: the 0-based, non-inclusive end position of the variant (i.e. _start_+1)
- **gene**: gene name
- **alt**: the alternative 3-mer
- **DP_AG**-**DS_DL**: Delta scores and positions, as described [here](https://github.com/Illumina/SpliceAI).
- **max_effect**: maximum across the different delta scores.


References:

```
@article{jaganathan2019predicting,
  title={Predicting splicing from primary sequence with deep learning},
  author={Jaganathan, Kishore and Panagiotopoulou, Sofia Kyriazopoulou and McRae, Jeremy F and Darbandi, Siavash Fazel and Knowles, David and Li, Yang I and Kosmicki, Jack A and Arbelaez, Juan and Cui, Wenwu and Schwartz, Grace B and others},
  journal={Cell},
  volume={176},
  number={3},
  pages={535--548},
  year={2019},
  publisher={Elsevier}
}

```
