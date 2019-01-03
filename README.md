# How to run the code in high-performance computing platform of SJTU Innovation Center
## Modify run.sh
- The second line is the name the job.
- The fifth line means all outputs will be written to the file log.%j.out.
- The fifth line means all errors will be written to the file log.%j.err. If there are no errors, then this file will be empty.
- The seventh line means that is the time limit of the job.
- The eightth line means the numbers of GPUs will be used to run the job.
- The last line is important. It is the command of how to run the train.py. You can use the following commands:
  - python train.py --dataset cifar10 --model wideresnet --data_augmentation --cutout --length 16
  - python train.py --dataset cifar10 --model resnet18 --data_augmentation --cutout --length 16
## Attention please
If the run.sh file is dos format, please use the command below to change it to unix format
```
dos2unix run.sh
```
## run the code
```
sbatch run.sh
```
# Introduction of models
## ResNet
![fig](https://github.com/ArtechStark/Cifar10-classification-WideResNet-and-cutout/blob/master/images/ResNet.png)
## WideResNet
![title](https://github.com/ArtechStark/Cifar10-classification-WideResNet-and-cutout/blob/master/images/WideResNet.png)
# Data augmentation
![title](https://github.com/ArtechStark/Cifar10-classification-WideResNet-and-cutout/blob/master/images/DataAugmentation.png)
# cutout
Cutout is a kind of regularization methods

![title](https://github.com/ArtechStark/Cifar10-classification-WideResNet-and-cutout/blob/master/images/cutout_on_cifar10.jpg)

#Training
## Comparison
![title](https://github.com/ArtechStark/Cifar10-classification-WideResNet-and-cutout/blob/master/images/comparison.png)
![title](https://github.com/ArtechStark/Cifar10-classification-WideResNet-and-cutout/blob/master/images/comparison2.png)
