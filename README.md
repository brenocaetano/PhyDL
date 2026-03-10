# PhyDL - Phylogram-based Data Labeling

This repository contains the implementation of the **PhyDL** algorithm, a novel approach that leverages phylogenetic structures for enhanced semi-supervised machine learning. Its performance is benchmarked against the **LLGC** (*Learning with Local and Global Consistency*) algorithm.

## 📋 Description

**PhyDL** (Phylogram-based Data Labeling) uses phylogenetic tree construction (Neighbor Joining) and the **Damicore** method to identify natural communities within datasets. By mapping labels onto these phylogenetic structures, it aims to achieve higher classification consistency and accuracy, especially in scenarios with extremely limited labeled data.

## 🚀 Key Features

* **LLGC Implementation**: A robust version of the Learning with Local and Global Consistency algorithm with stable symmetric normalization.
* **Damicore Integration**: Automated community detection using the `igraph` greedy algorithm on phylogenetic distances.
* **TSNE Visualizations**: Automatic generation of t-SNE plots to analyze the distribution of predicted vs. real labels.
* **Performance Metrics**: Automated calculation of Accuracy and F1-Score gains, exporting results to formatted CSV tables.

## 🛠️ Technologies and Dependencies

The project is developed in **Python 3.13+**. All required libraries can be installed via the provided `requirements.txt` file:

* `scikit-learn`: For preprocessing (`MinMaxScaler`), dimensionality reduction (`TSNE`), and evaluation.
* `python-igraph`: For graph manipulation and community detection.
* `biopython`: For building Neighbor Joining trees.
* `ete3`: For Newick tree file parsing.
* `ucimlrepo`: For automated access to UCI datasets (*Heart*, *Musk*, and *Sonar*).

## 📦 Installation

To set up your environment, run:

```bash
pip install -r requirements.txt
