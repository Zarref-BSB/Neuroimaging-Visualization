# Neuroimaging Visualization Project using Neurosynth Maps

**Author:** João Luís Silva Ferraz
**Date:** 30/11/2025
**Concept Source:** [Neurosynth: Memory](https://neurosynth.org/analyses/terms/memory/)

## Project Description
This project utilizes Python to automatically locate and visualize fMRI meta-analysis data obtained from Neurosynth, allowing the user to explore the concept of "Memory" or any other user-defined psychological term. It implements a reproducible pipeline that overlays functional statistical maps onto anatomical scans to highlight regions of significant brain activity. Furthermore, the script generates a histogram of positive Z-scores to visualize the distribution of voxel intensity for the chosen concept.

## Table of Contents and Data

This repository contains the following files and data sources:

 **`Neuroimaging Visualization.ipynb`** | The main Jupyter Notebook containing the Python code. It handles user input, automated file detection, plotting the statistical brain map, and generating the data histogram. |

 **`anatomical.nii.gz`** | High-resolution structural MRI scan (MNI152 template) used as the background for the visualization. |

 **`memory_uniformity-test_z_FDR_0.01.nii.gz`** | The functional data file downloaded from Neurosynth. It contains Z-scores representing the strength of association between brain activity and the term "Memory". |

 **`README.md`** | Documentation providing an overview of the project, dependencies, and file structure. |

> **Note:** To test different concepts, download the corresponding "uniformity test" map from [Neurosynth](https://neurosynth.org/), place it in this folder, and run the notebook.

## Dependencies

The following Python packages were used to create this project:

* **Python 3**
* **[Nilearn](https://nilearn.github.io/):** Used for plotting the statistical brain map (`plot_stat_map`).
* **[Nibabel](https://nipy.org/nibabel/):** Used for loading and manipulating the `.nii.gz` neuroimaging files and creating new NIfTI images.
* **[Matplotlib](https://matplotlib.org/):** Used for creating figures and plotting the histogram of Z-values.
* **[Numpy](https://numpy.org/):** Used for numerical operations and data filtering.
* **OS:** Standard Python library used for navigating the directory and locating files automatically.