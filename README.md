# CSE185Project t-SNE implementation
This is group 16 final project for CSE185. It follows the algorithm description in  the [original t-SNE parper](https://lvdmaaten.github.io/publications/papers/JMLR_2008.pdf) to implement t-SNE tool.

[![Python Version](https://img.shields.io/badge/python-3.6%20|%203.7%20|%203.8%20|%203.9%20|%203.10-blue.svg)](https://www.python.org/downloads/){:target="_blank"}


![PyPI Version](https://img.shields.io/pypi/v/your-package-name.svg)


# Table of contents <a name="toc"></a >
- [Sample Data Download](#data)
- [Installation Instructions](#install)
- [Basic Usage](#usage)
- [Complete Usage](#instruction)
- [Contributors](#credit)


# Sample Data Download <a name="data"></a>
[BACK TO TABLE OF CONTENTS](#toc)

Sample data (count matrix) taken from: 
[https://singlecell.broadinstitute.org/single_cell/study/SCP1526/functional-metabolic-and-transcriptional-maturation-of-human-pancreatic-islets-derived-from-stem-cells#study-download](https://www.ncbi.nlm.nih.gov/geo/download/?acc=GSE164073)
* need to make a Broad Institute account (Free!) to download the data


# Installation Instruction <a name="install"></a>
[BACK TO TABLE OF CONTENTS](#toc)

* Python Installation
[Click Me to Get Python](https://www.python.org/downloads/)

* Pip Installation 
```
python -m ensurepip --upgrade
```

* Installation requires the `numpy`, `pandas`, `matplotlib`, `scikit-learn` libraries to be installed. You can install these with `pip`:

```
pip install -r requirements.txt
```
* Once required libraries are installed, you can install `tsne` with the following command:
```
git clone https://github.com/m1ma0314/CSE185Group16_tSNE.git
cd CSE185Group16_tSNE
```

# Basic Usage <a name="usage"></a>
[BACK TO TABLE OF CONTENTS](#toc)

The basic usage of `my_tsne` is:
```
my_tsne.py [-p targer_perlexity] [-z ifzipped] [-o output] filename
```

To run `tsne` on a small test example (using files in this repo):

```
my_tsne.py -p 40 -z -o myplot minimal_dataset.csv
```
# Complete usage instructions <a name="instruction"></a>
[BACK TO TABLE OF CONTENTS](#toc)

The only required input to `my_tsne` is a cell x gene matrix data file. Users may additionally specify the options below:
* `-p PERPLEXITY`, `--target_perplexity PERPLEXITY`: specify perplexity between 5 and 50. If specified, the `tsne` function will calculate similarities matrix based on specified perplexity value and generate t-SNE plot. Higher perplexity value is associated with tighter clusters in the final output plot. Otherwise, the `tsne` function use `perplexity=40` by default.
* `-z ifzipped`, `--zipped`: unzip dataset file if this argument is specified. By default, the datafile is viewed as unzipped and will be converted into matrix for further processing.
* `-o FILE`, `--output FILE`: Write output to file. By default, output is written to `tsneplot.png`

## File Format
The output t-SNE plot is in `png` format.
![tsne_plot](https://github.com/m1ma0314/CSE185Group16_tSNE/assets/97704603/d9983cb9-58d6-416f-905b-bc62e580fb7c)

# Contributors <a name='credit'></a>
[BACK TO TABLE OF CONTENTS](#toc)

This repository was generated by Annabelle Coles and Mijia Ma, under the guidance of the [original t-SNE paper](https://lvdmaaten.github.io/publications/papers/JMLR_2008.pdf) and with inspiration from the article [t-SNE from scratch](https://towardsdatascience.com/t-sne-from-scratch-ft-numpy-172ee2a61df7)

Please submit a pull request with any corrections or suggestions. Your suggestions matter a lot to us <3


