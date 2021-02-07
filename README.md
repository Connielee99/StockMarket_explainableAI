# StockMarket_explainableAI
Contributing Members: 
- Sohyun Lee
- Shin Ehara
- Jou-Ying Lee

## Abstract
Deep learning architectures are now publicly recognized and repeatedly proven to be powerful in a wide range of high-level prediction tasks. While these algorithms’ modeling generally have beyond satisfactory performances with apposite tuning, the long-troubling issue of this specific learning lies in the un-explainability of model learning and predicting. This interpretability of “how” machines learn is often times even more important than ensuring machines outputting “correct” predictions. Especially in the field of finance, users’ ability to dissect how and why an algorithm reached a conclusion from a business standpoint is integral for later applications of i.e., to be incorporated for business decision making, etc. This project studies similar prior work done on image recognition in the financial market and takes a step further on explaining predictions outputted by the Convolutional Neural Network by applying the Grad-CAM algorithm. 

## Directory Structure
* **config**</br>
	This folder contains json files for main and testing parameters
	* `data_params.json`</br>contains parameters for running main on all data
	* `test_params.json`</br>contains parameters for running main on test data
* **data**</br>
	This folder contains all stock data from time series to image representation</br>
	
	**TSLA**</br>
	* RawData</br> This folder contains all obtained raw time series data
	* ProcData</br>This folder contains all processed csv files from RawData
	* TestData</br> This folder contains test target
	
	**imgs**</br>
	* all</br> This folder contains all images converted from time series
	* test</br> This folder contains test images converted by main
* **notebooks**</br>
	This folder is the notebook directory
	
	* `CNN_Model.ipynb`</br>is the development notebook for CNN implementation
	* `run_file.ipynb`</br>is the main development notebook that contains the same code as `run.py`
	
	**data_nb**</br>
	* `data_eda.ipynb`</br>is the notebook with eda work demonstration
	* `data_pipeline.ipynb`</br>is the notebook that wraps together data cleaning to feature engineering
	* `timeseries_convert_img`</br>is the notebook with image conversion work done
* **references**</br>
	This folder contains additional information/references in regards to our project
	
	**report_img**</br>
	* This folder contains images extracted from coded notebooks and included in the written report
* **src**</br>
	This folder contains library codes extracted from notebooks

	**data**</br>
		* `make_dataset.py`</br>scripts to prepare necessary data for this project
		
	**features**</br>
		* `build_features.py`</br>scripts to build features from merged data
		* `build_labels.py`</br>scripts to create labels for image classification
		* `build_images.py`</br>scripts to convert and save time series data to images
* **`Dockerfile`**</br>
	This is the dockerfile necessary to build the environment for this project development
* **`run.py`**</br>
	This is the main python file to execute our program
