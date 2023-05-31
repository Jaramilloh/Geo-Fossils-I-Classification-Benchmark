# Geo-Fossils-I-Classification-Benchmark

This repository contains the source code for a benchmark within the classification task for the [Geo Fossils-I Dataset](https://www.zenodo.org/record/7510741#.ZDfkf3ZBw2x) [1].


***Authors: Juan Felipe Jaramillo Hernández, María Fernanda Girón Arévalo***

Table of Contents
=================

<!--ts-->
   * [Architectures](#Architectures)
   * [Data Augmentation](#Data-Augmentation)
   * [References](#References)
<!--te-->

## Architectures

The following architectures were implemented with a classification head for the specific task:

* ResNet50
* InceptionV3
* Visual Transformer (b_16)
* Visual Transformer (b_32)

Each network were initialized with trained weights from the ImageNet [2] classification task, and each backbone is freezed, thus only applying gradient descent to the classification layer.


## Data Augmentation

In order to enhance the learning distribution space, the following data augmentation techniques were applied randomly for the images:

* Random resized crop.
* Random rotation.
* Color jitter.
* Random horizontal flip.
* Center crop.
* Standarization with  mean=[0.485, 0.456, 0.406] and std=[0.229, 0.224, 0.225].

## References

[1] Geo Fossils-I Dataset, available at https://www.zenodo.org/record/7510741#.ZHdI7RlBxki

[2] ImageNet: A large-scale hierarchical image database, available at https://ieeexplore.ieee.org/document/5206848
