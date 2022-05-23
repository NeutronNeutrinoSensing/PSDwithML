
# Improving Pulse Shape Discrimination in Organic Scintillation Detectors by Understanding Underlying Data Structure

by Patrick Maedgen, Benjamin Wellons, Shikha Prasad, and Jian Tao

Texas A&M University, College Station, Texas 77843-3133

The paper has been submitted for publication in Nuclear Technology.

This repository contains a Jupyter notebook and some sample data set to generate the results shown in the paper.


## Abstract

Various machine learning techniques have been implemented to assist in neutron-gamma
discrimination with great success compared to traditional methods. Despite this, the fundamental structure
of a pulse shape as it relates to machine learning has not yet been explored in detail, and the optimal
10 number of pulse vector features needed for training is still unknown. In this study, support vector machines
(SVMs) using linear, radial basis, and exponential kernel functions are fitted on data of two different forms:
waveforms that partially cover the original pulses and principal components extracted from those pulses.
The described methods correctly classified 98.02% for neutrons and 97.84% for gamma rays. The efficiency
of the SVM was improved by extracting principal components from the waveforms. That is, fewer features
15 were needed to discriminate between neutrons and gamma rays without negatively impacting the classifica-
tion accuracy. This study also shows that utilizing a nonlinear kernel significantly reduces the number of
features required to reach high classification accuracy. SVMs that did this could make accurate classifica-
tions 97% of the time with data that had fewer than 50 features.


## Software implementation

The calculations and figure generation are all run inside [Jupyter notebooks](http://jupyter.org/). 
The data used in this study is provided in `data`.


## Getting the code

You can download a copy of all the files in this repository with:

    git clone https://github.com/NeutronNeutrinoSensing/PSDwithML.git

or [download a zip archive](https://github.com/NeutronNeutrinoSensing/PSDwithML/archive/refs/heads/main.zip).

## Getting the data

Included in this repository is a sample dataset containing two csv files -- one containging neutron pulses, the other containing gamma pulses.
This data was processed and reformatted after being collected by CoMPASS. A time-of-flight cut has been applied prior, meaning there should be minimal overlap of neutrons and gammas.

Each file containins 500 columns: 496 samples for the given pulse with a resolution of 2 ns, the event index, pulse height, tail-to-total ratio, and a class label.
Neutrons are labelled as 1, gammas are labeled as 0. Each row represents an individual datapoint.

## License

All source code is made available under a [3-clause BSD license](https://opensource.org/licenses/BSD-3-Clause). You can freely
use and modify the code, without warranty, so long as you provide attribution to the authors.

