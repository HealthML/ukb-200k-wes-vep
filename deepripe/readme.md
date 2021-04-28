### DeepRiPe variant effect predictions

Variant effect predictions generated using the DeepRiPe convolutional neural network.

This model is described in here:

```
@article{ghanbari2020deep,
  title={Deep neural networks for interpreting RNA-binding protein target preferences},
  author={Ghanbari, Mahsa and Ohler, Uwe},
  journal={Genome research},
  volume={30},
  number={2},
  pages={214--226},
  year={2020},
  publisher={Cold Spring Harbor Lab}
}
```

Predictions are strand-specific, and were only produced vor variants overlapping protein-coding genes in the [Ensembl 97](https://www.ensembl.org/index.html) release. I.e. the predictions for chromosome X, strand Y can be found in `./chrX/Y_score.h5`. The accompanying file `./chrX/Y_vid.txt.gz` contains the variant names in the order they appear in the HDF5-datasets.

Every HDF5 file contains 3 datasets:
- `labels` containts the column names (corresponding to RBPs).
- `refscore` contains predictions for the reference alleles.
- `diffscore` containts the difference between predictions for the reference and alternative alleles.

Scores are only included if at least one "diffscore" had an absolute value greater or equal to 0.25.

Here is an example of how to load the data in python:

```
import h5py

with h5py.File('chr1/plus_scores.h5', 'r') as f:

    try:
        # in newer version of h5py the strings are not decoded -> decode them
        labels = [l.decode() for l in f['labels'][:]]
    except AttributeError:
        # this used to work in older versions of  h5py:
        labels = list(f['labels'][:])

    diffscores = infile['diffscore'][:]
    
```
