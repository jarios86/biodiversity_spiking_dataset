# Biodiversity Spiking Dataset

## Overview

This repository contains three IPYNB files for converting two classical datasets (audio and image) into spiking datasets. 
To do so, an artificial cochlea and an artificial retina simulator were used. 

## Requirements

For the audio conversion, a virtual environment with Python 3 is enough to run the [listening](https://github.com/jarios86/biodiversity_spiking_dataset/blob/main/listening.ipynb) file.

For the image conversion, an additional environment (with Python 2) is needed:
* The first [watching](https://github.com/jarios86/biodiversity_spiking_dataset/blob/main/watching_part_1.ipynb) file runs on Python 2;
* The second [watching](https://github.com/jarios86/biodiversity_spiking_dataset/blob/main/watching_part_2.ipynb) file runs on Python 3.

## Datasets

The datasets were (re)organized as follows.

For the audio conversion:

WABAD
- Recording site
  - Recordings
    - WAV
   Spikes
    - AEDAT

<directory_structure>
WABAD
└── Recording site
    ├── Recordings
    |   └── WAV
    └── Spikes
        └── AEDAT
</directory_structure>

For the image conversion: 

IBERBirds
- Images
  - Species
    - PNG
- Labels
  - Species
    - TXT
- Spikes
  - Spikes
    - AEDAT

