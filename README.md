# ERFNet (PyTorch version)

This code is a toolbox that uses **PyTorch** for training and evaluating the **ERFNet** architecture for semantic segmentation.

**For the Original Torch version please go [HERE](https://github.com/Eromera/erfnet)**

NOTE: This PyTorch version has a slightly better result than the ones in the Torch version (used in the paper): 72.1 IoU in Val set and 69.8 IoU in test set.

![Example segmentation](example_segmentation.png?raw=true "Example segmentation")

## Publications

If you use this software in your research, please cite our publications:

**"Efficient ConvNet for Real-time Semantic Segmentation"**, E. Romera, J. M. Alvarez, L. M. Bergasa and R. Arroyo, IEEE Intelligent Vehicles Symposium (IV), pp. 1789-1794, Redondo Beach (California, USA), June 2017. 
**[Best Student Paper Award]**, [[pdf]](http://www.robesafe.uah.es/personal/eduardo.romera/pdfs/Romera17iv.pdf)

**"ERFNet: Efficient Residual Factorized ConvNet for Real-time Semantic Segmentation"**, E. Romera, J. M. Alvarez, L. M. Bergasa and R. Arroyo, Transactions on Intelligent Transportation Systems (T-ITS), December 2017. [[pdf]](http://www.robesafe.uah.es/personal/eduardo.romera/pdfs/Romera17tits.pdf)

## Packages
For instructions please refer to the README on each folder:

* [train](train) contains tools for training the network for semantic segmentation.
* [eval](eval) contains tools for evaluating/visualizing the network's output.
* [imagenet](imagenet) Contains script and model for pretraining ERFNet's encoder in Imagenet.
* [trained_models](trained_models) Contains the trained models used in the papers. NOTE: the pytorch version is slightly different from the torch models.

## Requirements:

* [**The Cityscapes dataset**](https://www.cityscapes-dataset.com/): Download the "leftImg8bit" for the RGB images and the "gtFine" for the labels. **Please note that for training you should use the "_labelTrainIds" and not the "_labelIds", you can download the [cityscapes scripts](https://github.com/mcordts/cityscapesScripts) and use the [conversor](https://github.com/mcordts/cityscapesScripts/blob/master/cityscapesscripts/preparation/createTrainIdLabelImgs.py) to generate trainIds from labelIds**
* [**Python 3.6**](https://www.python.org/): If you don't have Python3.6 in your system, I recommend installing it with [Anaconda](https://www.anaconda.com/download/#linux)
* [**PyTorch**](http://pytorch.org/): Make sure to install the Pytorch version for Python 3.6 with CUDA support (code only tested for CUDA 8.0). 
* **Additional Python packages**: numpy, matplotlib, Pillow, torchvision and visdom (optional for --visualize flag)

In Anaconda you can install with:
```
conda install numpy matplotlib torchvision Pillow
conda install -c conda-forge visdom
```

If you use Pip (make sure to have it configured for Python3.6) you can install with: 

```
pip install numpy matplotlib torchvision Pillow visdom
```

## License

This work is licensed under a Creative Commons Attribution-NonCommercial 4.0 International License, which allows for personal and research use only. For a commercial license please contact the authors. You can view a license summary here: http://creativecommons.org/licenses/by-nc/4.0/
