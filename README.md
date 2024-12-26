# Astro Sonification: Approach to Astronomical Data Representation

## Abstract

This project presents a methodology for the sonification of galactic imagery, transforming visual data into an auditory format. By analyzing the red, green, and blue (RGB) pixel values of galaxy images, we establish a mapping between color and brightness characteristics and corresponding musical parameters, including melody, rhythm, and timbre. This approach offers a novel perspective on astronomical data exploration, facilitating a multi-sensory understanding of celestial structures.

## Project Scope

This repository provides a framework for the following functionalities:

*   **Data Acquisition:** Loading of galactic image data from a designated `.npy` file.
*   **Pixel-Level Analysis:** Extraction and analysis of RGB color information from the acquired images.
*   **Visual Representation:** Generation of image visualizations using OpenCV and matplotlib, complemented by heatmap generation for pattern identification.
*   **Data Serialization:** Export of extracted pixel data to a CSV file for subsequent computational analysis and processing.
*   **Auditory Transformation:** Implementation of a sonification algorithm that maps visual data to auditory parameters, specifically:
    *   Correlation of pixel brightness with auditory pitch.
    *   Modulation of auditory volume based on the red channel values.
    *   Determination of note duration based on the blue channel values.

## Sonification Mapping Protocol

1.  **RGB-Frequency Mapping:**

    The red, green, and blue components of each pixel are mapped to distinct frequency ranges, generating corresponding tonal characteristics:

    *   Red: Lower frequency spectrum.
    *   Green: Mid-frequency spectrum.
    *   Blue: Higher frequency spectrum.

    This process synthesizes a harmonic composition of sine waves, creating an auditory representation of the image's spectral content.

2.  **Luminosity-Pitch Correlation:**

    Pixel luminosity is directly correlated with auditory pitch:

    *   Increased luminosity corresponds to higher frequency values.
    *   Decreased luminosity corresponds to lower frequency values.

    This mapping facilitates an auditory representation of the image's light and shadow distribution.

3.  **Red Channel-Volume Modulation:**

    The intensity of the red channel is utilized to modulate auditory volume:

    *   Higher red channel values result in increased auditory amplitude.
    *   Lower red channel values result in decreased auditory amplitude.

4.  **Blue Channel-Duration Mapping:**

    The blue channel is employed to govern the temporal duration of auditory events:

    *   Lower blue channel values result in extended note durations.
    *   Higher blue channel values result in shortened, percussive note durations.

## Project Architecture

*   **data/:** Directory containing the galactic image dataset.
*   **.ipynb Notebooks:** Interactive computational notebooks containing the implemented code for image processing and sonification.
*   **output/:** Directory for the storage of extracted color data and generated visual outputs.
