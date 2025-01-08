# 🧬 Awesome RNA 3D structure prediction models
[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

</br>

Predicting the **3D structure** of **RNA molecules** is a challenging task due to limited training data and RNA specificities, but could lead to a better understanding of its functions and to the creation of new therapeutics. This repository aims to maintain a curated list of **awesome deep learning methods** to predict RNA 3D structure.

> Note that we do not include scoring functions or inverse folding methods, which are seen as a different topics.

> ⭐ Don't hesitate to open an issue or submit a pull request if you would like to add a paper or resource!

- [Databanks and datasets](#-databanks-and-datasets)
- [Models](#-models)
  - [2022](#-2022)
  - [2023](#-2023)
  - [2024](#-2024)

</br>

## 💾 Databanks and datasets

### Databanks

3D structures are generally optained from the [Protein Data Bank (PDB)](https://www.rcsb.org/). Challenging structures, generally used to evaluate models' performances can be found during the [RNA-Puzzles](http://www.rnapuzzles.org/) and [CASP15](https://predictioncenter.org/casp15/) challenges.

Some models use distillation to augment the data, since available RNA structures are limited. They often use the [bpRNA-1m](https://bprna.cgrb.oregonstate.edu/) database that contains annotated secondary structures.

### Datasets

Researchers often use their own methods to build datasets, separating between training and test sets based on sequence identity and thus not accounting for structural similarities.

- **RNA3DB** : a dataset created for machine learning training with train-test separation accounting for sequence and structural similarities. 

    [![](https://img.shields.io/badge/Paper-blue?logo=Read.cv&labelColor=grey)](https://www.sciencedirect.com/science/article/pii/S0022283624001475?via%3Dihub) 
    [![](https://img.shields.io/badge/Code-black?logo=GitHub&labelColor=grey)](https://github.com/marcellszi/rna3db)

</br>

## ✨ Models

### 📆 2022

- **DeepFoldRNA** : this model predicts simulation constraints with transformer-based blocks like AlphaFold 2, to guide energy minimization simulations that produce the structures.

    [![](https://img.shields.io/badge/Preprint-red?logo=Read.cv&labelColor=grey)](https://www.biorxiv.org/content/10.1101/2022.05.15.491755v1) 
    [![](https://img.shields.io/badge/Code-black?logo=GitHub&labelColor=grey)](https://github.com/robpearc/DeepFoldRNA)

- **RhoFold** : the first structure prediction method using deep learning only. Its architecture is close to AlphaFold 2 with transformers blocks and structure module. It uses of a foundation model for sequence embedding.

    [![](https://img.shields.io/badge/Preprint-red?logo=Read.cv&labelColor=grey)](https://arxiv.org/abs/2207.01586) 
    [![](https://img.shields.io/badge/Code-black?logo=GitHub&labelColor=grey)](https://github.com/Dharmogata/RhoFold)

### 📆 2023

- **epRNA** : this model predicts distances between pairs of residues from the sequence only using convolutionnal neurol networks. Refinement with force fields is used to obtain full-atom structures.

    [![](https://img.shields.io/badge/Paper-blue?logo=Read.cv&labelColor=grey)](https://www.sciencedirect.com/science/article/abs/pii/S0006349523006471) 
    [![](https://img.shields.io/badge/Code-black?logo=BitBucket&labelColor=grey)](https://bitbucket.org/dokhlab/eprna-euclidean-parametrization-of-rna/src/master/)
  
- **DRfold** : this method uses the sequence and predicted secondary structure to predict rotation/translation matrices and geometric constraints. Both are then used to guide an optimization process that leads to the structure.

    [![](https://img.shields.io/badge/Paper-blue?logo=Read.cv&labelColor=grey)](https://www.nature.com/articles/s41467-023-41303-9)
    [![](https://img.shields.io/badge/Code-black?logo=Github&labelColor=grey)](https://github.com/leeyang/DRfold)

- **NuFold** : an adaptation of AlphaFold 2's architecture to RNAs: frame definition and vocabulary changed, auxiliary networks added and templates replaced by secondary structure (predicted).

    [![](https://img.shields.io/badge/Preprint-red?logo=Read.cv&labelColor=grey)](https://www.biorxiv.org/content/10.1101/2023.09.20.558715v1) 
    [![](https://img.shields.io/badge/Code-black?logo=Github&labelColor=grey)](https://github.com/kiharalab/NuFold)

- **trRosettaRNA** : a transformer-based network similar to AlphaFold 2 which predicts 1D and 2D geometries used as constraints to guide folding based on energy minimization.

    [![](https://img.shields.io/badge/Paper-blue?logo=Read.cv&labelColor=grey)](https://www.nature.com/articles/s41467-023-42528-4)

- **RoseTTAFoldNA** : an adaptation of the RoseTTAFold2 model to predict protein-nucleic acid complexes. It updates 1D, 2D and 3D molecule representations that are fed into a SE(3) transformer and a model that predicts frame and rotation angles.

    [![](https://img.shields.io/badge/Paper-blue?logo=Read.cv&labelColor=grey)](https://www.nature.com/articles/s41592-023-02086-5)
    [![](https://img.shields.io/badge/Code-black?logo=Github&labelColor=grey)](https://github.com/uw-ipd/RoseTTAFold2NA)

### 📆 2024

- **Deep-RNAfold** : this models predicts distance classes using an autoregressive generative model with a VAE, Monte Carlo tree search (MCTS) and a scoring model.

    [![](https://img.shields.io/badge/Paper-blue?logo=Read.cv&labelColor=grey)](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0297105) 
    [![](https://img.shields.io/badge/Code-black?logo=Github&labelColor=grey)](https://github.com/ramakers/deep-rnafold)

- **AlphaFold 3** : the third iteration of Google's famous models, which includes multiple types of molecules and complexes (including RNA). It predicts atomic coordinates with a diffusion module.

    [![](https://img.shields.io/badge/Paper-blue?logo=Read.cv&labelColor=grey)](https://www.nature.com/articles/s41586-024-07487-w)
    [![](https://img.shields.io/badge/Code-black?logo=Github&labelColor=grey)](https://github.com/google-deepmind/alphafold3)

- **AutoRNA** : this method uses a VAE to predict distance matrices.

    [![](https://img.shields.io/badge/Preprint-red?logo=Read.cv&labelColor=grey)](https://www.biorxiv.org/content/10.1101/2024.06.18.599511v2) 
    [![](https://img.shields.io/badge/Code-black?logo=Github&labelColor=grey)](https://github.com/quantori/AutoRNA)

- **Rhofold+** : an improvement over Rhofold which keeps the same global architecture and features but uses a larger training dataset and a larger model with deeper attention modules.

    [![](https://img.shields.io/badge/Paper-blue?logo=Read.cv&labelColor=grey)](https://www.nature.com/articles/s41592-024-02487-0)
    [![](https://img.shields.io/badge/Code-black?logo=Github&labelColor=grey)](https://github.com/ml4bio/RhoFold)
  
- **Chai-1** : this model's architecture is really close to AlphaFold 3's, it predicts the structure of multiple molecules and complexes. RNA structures are predicted without MSA and one can add constraint features to guide the prediction.

    [![](https://img.shields.io/badge/Preprint-red?logo=Read.cv&labelColor=grey)](https://www.biorxiv.org/content/10.1101/2024.10.10.615955v2) 
    [![](https://img.shields.io/badge/Code-black?logo=Github&labelColor=grey)](https://github.com/chaidiscovery/chai-lab)
