# Semantic Segmentation
### Introduction
In this project, you'll label the pixels of a road in images using a Fully Convolutional Network (FCN).

### Setup
##### Frameworks and Packages
Make sure you have the following is installed:
 - [Python 3](https://www.python.org/)
 - [TensorFlow](https://www.tensorflow.org/)
 - [NumPy](http://www.numpy.org/)
 - [SciPy](https://www.scipy.org/)
##### Dataset
Download the [Kitti Road dataset](http://www.cvlibs.net/datasets/kitti/eval_road.php) from [here](http://www.cvlibs.net/download.php?file=data_road.zip).  Extract the dataset in the `data` folder.  This will create the folder `data_road` with all the training a test images.

### Start
The FCN implemented was based on this [paper](https://people.eecs.berkeley.edu/~jonlong/long_shelhamer_fcn.pdf). The neural network uses a vgg model where the dense layer is replaced with 1x1 convolutinal network, followed by up sampling and addition layers. The training was done on google cloud instance as it was computationally intensive and python instance crashed.

### Implementataion
The following hyper parameters were used
1. The learning rate was set to 0.0001. Higher learning rate yielded bad results
2. The keep probability(drop out) was set to 0.70 to prevent over fitting
3. The model was trained for 6 epoch and batch size was set to 16. Higher batch size caused resource exhaustion exception.


### Run
Run the following command to run the project:
```
python main.py
```
**Note** If running this in Jupyter Notebook system messages, such as those regarding test status, may appear in the terminal rather than the notebook.

### Results

The neural network successfully classified road pixels vs non road pixels. Some of the results are shown below

![Result 1](result/1.png?raw=true "Result 1")
![Result 2](result/2.png?raw=true "Result 2")
![Result 3](result/3.png?raw=true "Result 3")
![Result 4](result/4.png?raw=true "Result 4")
![Result 5](result/5.png?raw=true "Result 5")




 

