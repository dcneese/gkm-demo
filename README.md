# Exploring Regulatory Genomic Regions and Causal Variants with gkm-SVM and its Interpretive Methods

## Introduction
This project (a notebook with attached files) illustrates the power of the gkm-SVM classification method and several methods designed to interpret its results. The gkm-SVM is trained on intron regions in microglia and excitatory neurons that have been marked out as peaks in ATAC-Seq data. From this it is able to predict whether any input DNA sequence will act as an enhancer or promoter in a given cell type. Furthermore, we can estimate the effect of variants in these regulatory regions using gkmExplain, which generates a position weight matrix (PWM) to explain the contribution of each position in a sequence to its classification as an enhancer or a non-regulatory region. For a more readable writeup of results, see the attached pdf.

## Citations
The ls-gkm model used: https://github.com/Dongwon-Lee/lsgkm

The gkmExplain model used: https://github.com/kundajelab/gkmexplain

The sequence visualizer used: https://github.com/kundajelab/vizsequence

Additionally, code for this notebook was modified from the following demo notebooks for gkmExplain:
- https://github.com/kundajelab/gkmexplain/blob/master/lsgkmexplain_TALGATA.ipynb
- https://github.com/kundajelab/gkmexplain/blob/master/lsgkmexplain_Nanog.ipynb

## Rough Outline of the Notebook
- Import and subset data
- Train the gkm-SVM models
  - train one model for each cell type/cluster
- Test the models
  - obtain precision, recall, ROC AUC
- Analyze example output
  - show gkmExplain output and relation to motifs
  - show effect of variants on classification
  - show limited applicability of models across cell types
