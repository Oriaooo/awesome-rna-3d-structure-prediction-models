<h1 align="center">
🧬 Awesome RNA 3D structure prediction models
</h1>

<div align="center">
[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
</div>

Predicting the **3D structure** of **RNA molecules** is a challenging task due to limited training data and RNA specificities, but could lead to a better understanding of its functions and to the creation of new therapeutics. This repository aims to maintain a curated list of **awesome deep learning methods** to predict RNA 3D structure. 

<pre>⭐ Don't hesitate to open an issue or submit a pull request if you would like to add a paper or resource!</pre>

- [Databanks and datasets](#-databanks-and-datasets)
- [Models](#-models)

## 💾 Databanks and datasets

### Databanks

3D structures are generally optained from the [Protein Data Bank (PDB)](https://www.rcsb.org/). Challenging structures, generally used to evaluate models' performances can be found during the [RNA-Puzzles](http://www.rnapuzzles.org/) and [CASP15](https://predictioncenter.org/casp15/) challenges.

Some models use distillation to augment the data, since available RNA structures are limited. They often use the [bpRNA-1m](https://bprna.cgrb.oregonstate.edu/) database that contains annotated secondary structures.

### Datasets

Researchers often use their own methods to build datasets, separating between training and test sets based on sequence identity and thus not accounting for structural similarities.

- **RNA3DB** : a dataset created for machine learning training with train-test separation accounting for sequence and structural similarities. 
[![](https://img.shields.io/badge/Paper-5291C8?logo=Read.cv&labelColor=555555)](https://www.sciencedirect.com/science/article/pii/S0022283624001475?via%3Dihub)
[![](https://img.shields.io/badge/code-38C26D?logo=GitHub&labelColor=555555)](https://github.com/marcellszi/rna3db)

## ✨ Models