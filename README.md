# Biodiversity Spiking Dataset

## Overview

This repository contains three IPYNB files for converting two classical datasets (audio and image) into spiking datasets. 
To do so, an artificial cochlea (NAS) and an artificial retina simulator ([ESIM](https://github.com/uzh-rpg/rpg_esim)) were used, respectively. 

## Requirements

For the audio conversion, a virtual environment with Python 3 is enough to run the [listening](https://github.com/jarios86/biodiversity_spiking_dataset/blob/main/listening.ipynb) file.

For the image conversion, an additional environment (with Python 2) is needed:
* The first [watching](https://github.com/jarios86/biodiversity_spiking_dataset/blob/main/watching_part_1.ipynb) file runs on Python 2.
* The second [watching](https://github.com/jarios86/biodiversity_spiking_dataset/blob/main/watching_part_2.ipynb) file runs on Python 3.

## Datasets

The datasets were (re)organized as follows.

For the audio conversion:

```
WABAD
└── Recording site
    ├── Recordings
    |   └── WAV
    └── Spikes
        └── AEDAT
```

- **WABAD** is the root folder of the dataset.
- **Recording site** contains different folders (that do not indicate the species). 
- **Recordings** is the folder with the original audio files in WAV format.
- **Spikes** is the folder with event-based files in AEDAT format.

For the image conversion: 

```
IBERBirds
├── Images
|   └── Species
|       └── PNG
├── Labels
|   └── Species
|       └── TXT
├── Sequences
|   └── Species
|       └── Birds
|           └── cam0
|               └── frames
|                   ├── PNG
|                   └── timestamps.CSV
├── Bags
|   └── Species
|       └── Birds
|           └── Out
|               ├── cam0-events.CSV
|               └── out.BAG
└── Spikes
    └── Species
        └── AEDAT
```

- **IBERBirds** is the root folder of the dataset.
- **Images** contains subfolders for each specie, where the original images are stored in PNG format.
- **Labels** contains subfolders for each specie, with corresponding label files in TXT format.
- **Sequences** contains subfolders for each specie and each bird, with the generated frame sequences in PNG format and the corresponding timestamps in a CSV file.
- **Bags** contains subfolders for each species, including CSV files and BAG files related to each bird.
- **Spikes** contains subfolders for each specie, where the event-based (spiking) files are stored in AEDAT format.

Please ensure any new dataset follows the same structure before using the scripts. 

## Checks

Before converting a whole dataset, it could be usefult to visualize some useful graphs.

Before the audio conversion, it is possible to confront up to 5 different graphs before and after saving the events in a new AEDAT file, in order to check if they are saved correctly. 

Before the image conversion, it is possible to visualize the events integrated either by time or by number of events. In both cases, the result is a sequence of images that resemble the output of the simulator (that works with the corrisponding BAG files). 
