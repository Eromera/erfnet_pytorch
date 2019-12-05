# Imagenet pretraining script and model

This folder contains the script and model definition to pretrain ERFNet's encoder in Imagenet Data. 

The script is an adaptation from the code in [Pytorch Imagenet example](https://github.com/pytorch/examples/tree/master/imagenet). Please make sure that you have Imagenet dataset split in train and val folders before launching the script. Refer to that repository for instructions about usage and main.py options. Basic command:

```
python main.py <imagenet_folder_path>
```
