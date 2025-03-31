# Deep Learning in PAMGuard Tutorial

## Introduction
This tutorial is a step by step guide to on how to run deep learning models in PAMGuard. The tutorial takes users through how to set up a configuration, process data and classify to species using three examples, North Atlantic Right whales, bats in Denmark and gibbons in Laos.

## Species

- North Atlantic Right whale (Eubalaena glacialis)
- Danish bat species (Pipistrellus pygmaeus, Nyctalus noctula, Eptesicus serotinus, Myotis nattereri and Myotis daubentonii)
- Northern white-cheeked gibbon (Nomascus leucogenys)

## What you will learn
### Section 1 - Right whales
In section 1, you will be shown how to process raw low frequency sound files to detect North Atlantic Right whale upsweeps using a deep learning model developed by Shiu et al, (2020). This model was trained on a widely available dataset used to test automated classifiers for right whales and was a significant improvement on previous methods. The end of the tutorial compares the deep learning model against a more heuristic Right whale classifier built into PAMGuard. Users will also learn how to export deep learning detections to MATLAB, R and wav files.

### Section 2 - Bats
Section 2 deals with much higher frequency sound files (384kHz) recorded by an AudioMoth near woodland in Denmark. The sound files contain a large number of bat calls from different species, primarily Myotis daubentonii and Pipistrellus pygmaeus An AnimalSpot model from Brinkløv et al, (2023) has been supplied which classifies bat calls based on a segment of sound data around one thousand samples in length. However, it takes around 10-100ms to run a single segment through the classification algorithm and there are at least 384 non-overlapping chunks in one second of data. Some basic maths and that shows that this classifier will run well below real time. To address this, users will use PAMGuard to run a very simple bat detector and then run the deep learning model on the detected data rather than all the raw data.

### Section 3 - Gibbons
In section 3 you will learn how to integrate the deep learning into a workflows in PAMGuard. We use some example of Gibbon calls detected by a 4 channel recorder in Laos. The 4 channel recorder can be determine a bearing to call - the output of the deep learning module is connected with the bearing module so that any classified call is localized. Although not part of the tutorial, the end goal of this project was to use the bearings to monitor the abundance of gibbons in the forest.

## Downloads

The tutorial text is in Deep learning in PAMGuard 2022-v1-2-12-16.pdf You will also need to download the accompanying data sets from Zenodo.

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.13880107.svg)](https://doi.org/10.5281/zenodo.13880107) - **Right whale data set**

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.15045544.svg)](https://doi.org/10.5281/zenodo.15045544) - **Bat data set**

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.15045966.svg)](https://doi.org/10.5281/zenodo.15045966) - **Gibbon data set**
