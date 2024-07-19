# Code for "Towards flexible perception with visual memory"

This repository contains code to replicate experiments from "Towards flexible
perception with visual memory" by Robert Geirhos, Priyank Jaini, Austin Stone,
Sourabh Medapati, Xi Yi, George Toderici, Abhijit Ogale, and Jonathon Shlens.

## Setup
The `code/` directory contains two `.ipynb` notebooks. They depend on common
libraries like numpy and jax, but do not require installing packages.

## Overview
[![nearest_neighbor_evaluation.ipynb](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/google-deepmind/visual_memory/blob/master/code/nearest_neighbor_evaluation.ipynb) The colab `nearest_neighbor_evaluation.ipynb` extracts nearest neighbor information from
running datasets like ImageNet and stores the results as `.JSON` files just like the ones listed below under `Evaluation data`.

[![main_analysis_plots.ipynb](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/google-deepmind/visual_memory/blob/master/code/main_analysis_plots.ipynb) The colab `main_analysis_plots.ipynb` reads those `.JSON` files, analyzes and plots the results.

For more details see the methods section of our paper, and please feel free to
open an issue or reach out in case anything is unclear.

## Evaluation data
Nearest neighbor information for CLIP and DinoV2 models is provided as JSON files for download [here](https://console.cloud.google.com/storage/browser/visual_memory_v01). The JSONs have the following structure:

`featurizer`: model name<br>
`image_id`: ID of test image<br>
`image_class`: class of test image<br>
`neighbor_image_ids`: list of nearest neighbor image IDs<br>
`neighbor_classes`: list of class of nearest neighbors<br>
`neighbor_distances`: list of distance to nearest neighbors<br>

And the filename indicates the dataset used for memory and testing, respectively, as well as the split (train/test).

## Citation
```
@article{geirhos2023fooling,
  url = {https://arxiv.org/abs/TBD},
  author = {Geirhos, Robert and Jaini, Priyank and Stone, Austin and Medapati, Sourabh and Yi, Xi and Toderici, George and Ogale, Abhijit and Shlens, Jonathon},
  title = {Towards flexible perception with visual memory},
  journal={arXiv preprint arXiv:TBD},
  year = {2024},
```

## License and disclaimer
Copyright 2024 DeepMind Technologies Limited
All software is licensed under the Apache License, Version 2.0 (Apache 2.0);
you may not use this file except in compliance with the Apache 2.0 license.
You may obtain a copy of the Apache 2.0 license at:
https://www.apache.org/licenses/LICENSE-2.0
All other materials are licensed under the Creative Commons Attribution 4.0
International License (CC-BY). You may obtain a copy of the CC-BY license at:
https://creativecommons.org/licenses/by/4.0/legalcode
Unless required by applicable law or agreed to in writing, all software and
materials distributed here under the Apache 2.0 or CC-BY licenses are
distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND,
either express or implied. See the licenses for the specific language governing
permissions and limitations under those licenses.

This is not an official Google product.

