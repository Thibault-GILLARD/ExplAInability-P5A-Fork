
# TASSEL_orig
<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="http://umr-tetis.fr/index.php/fr">
  <img src="https://www.teledetection.fr/images/programs/programs-thumb2-TETIS.jpg" alt="Logo" style="width: 40%;">
</a>
  <h2 align="center">Weakly Supervised Learning for Land Cover
Mapping of Satellite Image Time Series via
Attention-Based CNN
TASSEL_orig</h3>
  <a href="https://www.epf.fr/en">
    <img src="https://upload.wikimedia.org/wikipedia/fr/e/e9/EPF_logo_2021.png" alt="Logo" width="211" height="179">
  </a>
  <p align="center">
    Code developed for the web programming course at epf whose goal was "Create your own APIs to share data".
    <br />
    <a href="https://github.com/pierrert3/ExplAInability-P5A/tree/main"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/pierrert3/ExplAInability-P5A/issues">Report Bug</a>
    <a href="https://github.com/pierrert3/ExplAInability-P5A/issues">Request Feature</a>
  </p>
</div>

<!-- ABOUT THE PROJECT -->
## About The Project

- **Objective of the article** : [Link to article](https://hal.inrae.fr/hal-02941804)

The use of time series of high-resolution satellite images opens up new opportunities for monitoring the earth's surface, but also poses challenges in terms of analysing massive amounts of data. One of these challenges concerns land cover mapping, where the information available is often limited and of approximate quality. To address this challenge, the authors propose TASSEL, a new deep learning framework that exploits detailed information from satellite images to improve land mapping. Their experiments show that TASSEL not only improves predictive performance compared with competing approaches, but also provides additional information for interpreting model decisions.

<!-- MAP VIEW -->
## MAP VIEW

GOOGLE API
https://explainability-tassel.github.io/ExplAInability-P5A/

MapBox API
https://thibault-gillard.github.io/Explainability/

![Alt Text](https://github.com/pierrert3/ExplAInability-P5A/blob/main/assets/Enregistrement%20de%20l%E2%80%99%C3%A9cran%202023-09-22%20%C3%A0%2023.52.46.gif)


## Organization of the project

This project is organized into several key files and directories:

### 1. Preprocessing

The preprocessing is done in the numbered notebooks, following the numerical order :
- `1_data_analyze.ipynb` analyze the input data.
- `2_extract_included_segments.ipynb` extract segments partially (0%->100%) included in polygons for training set.
- `2_extract_segments.ipynb` extract all segments and their pixels for inference set.
- `3_segment_analyze.ipynb` analyze the segment extraction results.
- `4_normalization.ipynb` normalize the acquisition data.
- `5_730_conversion.ipynb` convert pixel coordinates for each segment (obtained with `2_extract_segments.ipynb`) to their 730 values vector (73 acquisitions for 10 bands --> 730 values).

The requiered packages are listed in the `requirements.txt` file.

The preprocessing can also be done with the `preprocessing.py` file, hence can be launched with a command line.



### 2. Training and Inference

- `main_inference.ipynb` and `main_train.ipynb`: These Jupyter notebooks contain the main code for training and inference.

- `model_components/`: This directory contains the source code for the model components. It includes:

  - `Attention_Layer.py`: Implements an attention layer for a neural network.

  - `CNN_model.py`: Implements a Convolutional Neural Network (CNN) model.

  - `classification.py`: Implements a classification model.

  - `k_means.py`: Implements a k-means clustering algorithm.

  - `test_K_m.py`: Contains tests for the k-means clustering algorithm.

### 3. The Map

- `index.html`: This file contains the code for the map.

- `sources/`: This directory contains the source code for the map. It includes:

  - `data.json`: Contains the data for the map.
  - `segment_lat_long.json`: Contains the data for the map.

## Installation

Python 3.10.13 was used for this project.

1. Clone the repo
   ```sh
   git clone https://github.com/pierrert3/ExplAInability-P5A.git
    ```
2. Install the required packages
    ```sh
    pip install -r requirements.txt
    ```
3. Run the notebooks to train and test the model
4. Run the map
5. If you want to use the map with your own data, you can use the `index.html` and `segment_lat_long.json` file as a template.
  
<!-- Authors -->
## Authors

- [GAUBIL Clara (@claragbl)](https://github.com/claragbl)
- [GILLARD Thibault (@Thibault-GILLARD)](https://github.com/Thibault-GILLARD)
- [COURBI Antoine (@TonioElPuebloSchool)](https://github.com/TonioElPuebloSchool)
- [RAGEOT Pierre (@pierrert3)](https://github.com/pierrert3)

Publication authors:

- RAFFAELE GAETANO
- DINO IENCO
- YAWOGAN JEAN EUDES GBODJO
- ROBERTO INTERDONATO

<!-- LICENSE -->
## License

Distributed under the 'GNU GENERAL PUBLIC LICENSE' License. See `LICENSE` for more information.
