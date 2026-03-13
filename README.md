# Beta-sheet analysis pipeline
This repository contains the JIPipe pipeline used for analyzing β‑sheet fluorescence microscopy images.

# Summary
This project implements an image analysis pipeline for quantifying fluorescence coverage of ß-sheets on circular titanium disks from tiled fluorescence microscopy images. Raw . czi microscopy files are processed to extract tiles. A mask needs to be created manually once the pipeline automatically requests it. This help restricts the analysis to the disk surface. Fluorescent structures are segmented within the disk using a consistent thresholding approach, where the threshold were extracted from negative control images. The final output provides coverage measurements across the experimental conditions. The result table has two columns one for the file name and one for the surface coverage value as a percentage.

# Description
Description

The image analysis pipeline requires  JIPipe 6.0.0 and Python for processing the images. The workflow uses the ImageJ plugin BaSiC, which must be installed via the ImageJ Update Manager before running the pipeline.

The Python environment (Python 3.11) includes the following libraries:

NumPy 2.4.0
Pandas 3.0.1
Matplotlib 3.10.8
Seaborn 0.13.2
aicspylibczi 3.3.1 (for reading Zeiss CZI microscopy files)

These dependencies are provided through the included environment.yml to ensure a reproducible analysis environment.
