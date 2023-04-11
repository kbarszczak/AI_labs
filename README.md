![banner](https://user-images.githubusercontent.com/72699445/231169044-b3b38f22-ace1-482b-b200-e6758964f620.png)
This repository contains various artificial intelligence projects. All of them are made as university projects.

# TSD (Traffic sign detection)

The project shows how the combination of CNN (convolutional neural networks) and sliding window method may be used to detect signs in the images. This is the simplest detection method so it takes around a few minutes on average to detect signs.

The CNN classifier detects 43 different classes of signs. The progress of improving the AI models that classify the signs is shown in notebooks in the directory TSD_project/model/.* and in the TSD_project/TSD_CNN_presentation.pdf file.

## Usage

First of all, install all the packages from the requirements.txt file
```
pip install -r requirements.txt

```
Then clone the repository to the proper directory
```
mkdir AI_labs
cd AI_labs
git clone https://github.com/kbarszczak/AI_labs .
```
If you have a GPU configured now is the proper time to activate it. In my case simply by doing:
```
conda activate tensorflow-gpu
```
After cloning the repository run the jupyter notebook
```
jupyter notebook
```
Then go to any of the notebooks from TSD_project/model/ and run: kernel -> restart and run all
Email me to get the preprocessed training dataset.

To test the system run the following notebook: TSD_project/env/SW_ENV_V1.ipynb set up paths to the AI model and the test photo and run all.
The result is going to be presented in the last cell.

## Possible improvements
The following may be improved in this project:
- The conflict elimination algorithm in the SW_ENV_V1.ipynb notebook. Sometimes it merges the objects that should be splitted
- Training models on data processed in a better way (eg. CLAHE on training dataset - it is already done but the results are not presented)
- Implement a better technique than sliding window (eg. try to detect objects in a circular shape and send only those for the classifier)
