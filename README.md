# Biosignal Processing and Analysis Course Project
- [About The Project](#about-the-project)
- [Getting Started](#getting-started)
  * [Convert the dataset](#convert-the-dataset)
  * [Get basic plots and info](#get-basic-plots-and-info)
  * [Preprocessing](#preprocessing)
  * [Feature Selection](#feature-selection)
  * [Models](#models)

## About the project
This project is a part of Biosignal Processing and analysis Course Project and aims to predict driver stress levels using Physionet's [SRAD](https://physionet.org/content/drivedb/1.0.0/) (drivedb) dataset with methods such as LSTMs, RNNs and CNNs.
The dataset contains inputs collected from physiological signals such as: **Electrocardiogram, Electromyogram, and Galvanic Skin Response.**

## Getting started
The scripts are sorted in an alphabetical manner to make it easier for anyone to run the codes. Hence, if one is interested in running the `c_preprocessing.py` script, the data has to be provided as in the proceding scripts, i.e: `a_convert_to_csv.py`.

### Convert the dataset
To convert the files from .dat format to csv, you can run the `a_convert_to_csv.py` file. This can be done by calling the `convert_to_csv` function with default parameters.

### Get basic plots and info
To plot the data for each drive, the `b_basic_information.py` script can be utilized.

### Preprocessing
The initial dataset does not contain the marker data. To attach the marker data to each csv, the `process_data` function from `c_preprocessing.py` script can be used.

### Feature Selection
The dataset consists of 7 columns, namely: *ECG, EMG, hGSR, fGSR, HR, RESP*. To create a set of 22 features, `d_feature_selection.py` can be run which will create the following columns: **EMG_mean, footGSR_mean, footGSR_std, footGSR_frequency, footGSR_magnitude, footGSR_duration, footGSR_area, handGSR_mean,handGSR_std, handGSR_frequency,	handGSR_magnitude, handGSR_duration, handGSR_area, HR_mean,	HR_std, HRV_ratio, RESP_mean, RESP_std, RESP_ulf, RESP_vlf, RESP_lf, RESP_hf, Stress.**\
Moreover, the data can be segmented into different intervals. The default value is 10 seconds.

### Models
Lastly, this project aims to predict stress levels using various reduction techniques with the aid of deep learning models such as LSTMs, CNN and RNNs. These techniques can be accessed in the `e_models.py` file.


### Feature Selection Infographics
Galvanic Skin Response Features
![Screenshot](/img/gsr-features.png)

Heart Rate Features
![Screenshot](/img/hr-features.png)

Resp Features
![Screenshot](/img/resp-features.png)

