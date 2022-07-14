# IDC-Prostate_segmentation
Prostate segmentation task on IDC collections

<div id="top"></div>

<!-- TABLE OF CONTENTS -->
<!--
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>
-->
<!-- ABOUT THE PROJECT -->
## About The Project

The goal of this project is to augment IDC collections with DL based segmentation masks obtain from nnU-net framework, using pre-trained models inference on IDC collections. 

Two nnU-net based pre-trained models have been used for inference on two different IDC collections.

The pre-trained models, Task005-Prostate(PZ and TZ) and Task024-Promise(whole prostate) can be found/downloaded in [Zenodo](https://zenodo.org/record/4003545#.YtCHOOzMJqs).

The two labelled IDC collections are [ProstateX](https://portal.imaging.datacommons.cancer.gov/explore/filters/?collection_id=prostatex) and [QIN-PROSTATE-Repeatability](https://portal.imaging.datacommons.cancer.gov/explore/filters/?collection_id=qin_prostate_repeatability).

The nnU-net architecture model chosen is 3d_fullres across all experiments, with test-time data augmentation enabled.
Task024 has only one input modality, T2, whereas Task005 is multi-modal, T2 and ADC.

<!-- <p align="right">(<a href="#top">back to top</a>)</p -->

<!-- GETTING STARTED -->
## Getting Started

All these ipynb were run through google colab.

### Prerequisites

* [Google account](https://accounts.google.com/signup/v2/webcreateaccount?flowName=GlifWebSignIn&flowEntry=SignUp)
* [IDC Documentation](https://learn.canceridc.dev/) 
  * [Google Cloud Project](https://learn.canceridc.dev/introduction/getting-started-with-gcp#set-up-a-google-cloud-project)
  * [Enable gcp BigQuery API](https://learn.canceridc.dev/introduction/getting-started-with-gcp#enable-gcp-bigquery-api)

### Notebooks -- Getting started

Below is detailed description of the structure of the repository :

1. [**Notebooks folder**](https://github.com/ccosmin97/IDC-Prostate_segmentation/tree/main/IDC_notebooks)
    * [idc-prostate_segmentation_promised24_QIN-PROSTATE-Repeatability.ipynb](https://github.com/ccosmin97/IDC-Prostate_segmentation/blob/main/IDC_notebooks/idc-prostate_segmentation_promised24_QIN-PROSTATE-Repeatability.ipynb) : Experiment on QIN-PROSTATE-Repeatability using pre-trained model Task024-Promise.
    * [idc-prostate_segmentation_promised24_prostateX.ipynb](https://github.com/ccosmin97/IDC-Prostate_segmentation/blob/main/IDC_notebooks/idc-prostate_segmentation_promised24_prostateX.ipynb) : Experiment on ProstateX using pre-trained model Task024-Promise.
    * [idc-prostate_segmentation_prostate05_qin-rep-repeat.ipynb](https://github.com/ccosmin97/IDC-Prostate_segmentation/blob/main/IDC_notebooks/idc-prostate_segmentation_prostate05_qin-rep-repeat.ipynb) : Experiment on Qin-Prostate-Repeatability using pre-trained model Task005-Prostate computing evaluation metrics on Peripheral Zone of the prostate only
    * [results_analysis.ipynb](https://github.com/ccosmin97/IDC-Prostate_segmentation/blob/main/IDC_notebooks/results_analysis.ipynb) : Results analysis from experiments
2. [**nnunet_results**](https://github.com/ccosmin97/IDC-Prostate_segmentation/tree/main/nnunet_results) : Contains the DSC and other quantitative metrics results for each experiment, used also in results_analysis.ipynb 

3. Open any of these ipynb in colab!
<!--
   ```sh
   npm install
   ```
4. Enter your API in `config.js`
   ```js
   const API_KEY = 'ENTER YOUR API';
   ```
<p align="right">(<a href="#top">back to top</a>)</p>
-->
