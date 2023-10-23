# Genetic Language Distance Calculator

## Overview

This Python project aims to calculate genetic distances between languages based on the Glottolog hypothesized tree of languages. The genetic distance metric is defined as the number of steps upward on the tree until two languages are unified under a single node, divided by the number of branches in between Language 1 and the root. This metric represents the percentage of L1's descent not shared by Language 2. The calculation is quoted from the description provided by Prof. David Mortensen's [website](https://www.cs.cmu.edu/~dmortens/projects/7_project/).

## Motivation

The motivation for this project stems from the need to calculate genetic distances between languages, an important task in linguistics and language-related research. Although lang2vec is a popular tool in this field, it lacks transparency in how genetic distances are calculated. In addition, the methodology used by lang2vec is not explicitly described in its paper, and the results appear to be somewhat erroneous.


## Features

- Calculate genetic distances based on the Glottolog hypothesized tree of languages.
- Intuitive distance metric that represents the percentage of L1's descent not shared by L2.
- Provides better language genetic distances.
- Outputs distance metrics in a structured format for further analysis.

## Usage

To use this project, you can follow these steps:

1. Download [this](https://cdstar.eva.mpg.de//bitstreams/EAEA0-B701-6328-C3E3-0/glottolog_languoid.csv.zip) CSV file containing language information.
2. Download [this](https://cdstar.eva.mpg.de//bitstreams/EAEA0-B701-6328-C3E3-0/tree_glottolog_newick.txt) Newick tree structure into a txt format file.
3. Substitue the file paths of these two files with you paths.
4. Provide a list of Glottolog language names that you wish to study. To check if a language is supported by Glottolog, search in the Name entry [here](https://glottolog.org/glottolog/language)
5. Run through the code and then use the `get_distance` function to calculate genetic distances between languages.
6. Access the calculated distances for your analysis or research.

## Results

This method for calculating genetic distances has yielded dissimilarity matrices that are more intuitive and accurate when compared to the results obtained from lang2vec. 

The dissimilarity matrix is a powerful tool for comparing languages and understanding their genetic relationships, which is a quick tool for sanity check and comparison. Languages from the same top level language families should have a lower dissimilarity score. You can explore and analyze the dissimilarity matrix in the notebook by providing a list of language families you wish to investigate.

Here is the Indo-European language dissimilarity matrix calculated according to lang2vec genetic distance:

![lang2vec result](https://github.com/qinwenshuo/Genetic-Distance/assets/53549553/38a0a4cd-1ace-4e86-953e-d80f8ccf2032)

Here is the Indo-European language dissimilarity matrix calculated according to this project's code:

![download (4)](https://github.com/qinwenshuo/Genetic-Distance/assets/53549553/68ab0db4-bc4e-456e-89d6-40e654bbaba6)

More comparison can be seen here:

[lang2vec](https://docs.google.com/document/d/14KpmoXCsTp3acAJLDcs2UKHidksYJ4XsWATU6SRgoGs/edit?usp=sharing)

[this project](https://docs.google.com/document/d/171tgUBvQ-6iWdNexMXjAxPrsr8qZt_-MEBB5dPufmkI/edit?usp=sharing)

## References

- [Glottolog](https://glottolog.org/): The Glottolog database and tree of languages were used as a basis for this project.

- [Prof. David Mortensen's Website](https://www.cs.cmu.edu/~dmortens/projects/7_project/): The methodology for calculating genetic distances is inspired by the description provided by Prof. David Mortensen.

- [lang2vec](https://github.com/antonisa/lang2vec): lang2vec is a widely used tool for calculating language vectors and related metrics.

