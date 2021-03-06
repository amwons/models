<!--- SPDX-License-Identifier: BSD-3-Clause -->

# AlexNet

|Model        |Download  |Download (with sample test data)| ONNX version |Opset version|
| ------------- | ------------- | ------------- | ------------- | ------------- |
|AlexNet| [238 MB](model/bvlcalexnet-3.onnx)  |  [225 MB](model/bvlcalexnet-3.tar.gz) |  1.1 | 3|
|AlexNet| [238 MB](model/bvlcalexnet-6.onnx)  |  [225 MB](model/bvlcalexnet-6.tar.gz) |  1.1.2 | 6|
|AlexNet| [238 MB](model/bvlcalexnet-7.onnx)  |  [226 MB](model/bvlcalexnet-7.tar.gz) |  1.2 | 7|
|AlexNet| [238 MB](model/bvlcalexnet-8.onnx)  |  [226 MB](model/bvlcalexnet-8.tar.gz) |  1.3 | 8|
|AlexNet| [238 MB](model/bvlcalexnet-9.onnx)  |  [226 MB](model/bvlcalexnet-9.tar.gz) |  1.4 | 9|

## Description
AlexNet is the name of a convolutional neural network for classification,
which competed in the ImageNet Large Scale Visual Recognition Challenge in 2012.

Differences:
- not training with the relighting data-augmentation;
- initializing non-zero biases to 0.1 instead of 1 (found necessary for training, as initialization to 1 gave flat loss).

### Paper
[ImageNet Classification with Deep Convolutional Neural Networks](https://papers.nips.cc/paper/4824-imagenet-classification-with-deep-convolutional-neural-networks.pdf)

### Dataset
[ILSVRC2012](http://www.image-net.org/challenges/LSVRC/2012/)

## Source
Caffe BVLC AlexNet ==> Caffe2 AlexNet ==> ONNX AlexNet

## Model input and output
### Input
```
data_0: float[1, 3, 224, 224]
```
### Output
```
softmaxout_1: float[1, 1000]
```
### Pre-processing steps
### Post-processing steps
### Sample test data
Randomly generated sample test data:
- test_data_0.npz
- test_data_1.npz
- test_data_2.npz
- test_data_set_0
- test_data_set_1
- test_data_set_2

## Results/accuracy on test set
The bundled model is the iteration 360,000 snapshot.
The best validation performance during training was iteration
358,000 with validation accuracy 57.258% and loss 1.83948.
This model obtains a top-1 accuracy 57.1% and a top-5 accuracy
80.2% on the validation set, using just the center crop.
(Using the average of 10 crops, (4 + 1 center) * 2 mirror,
should obtain a bit higher accuracy.)

## License
[BSD-3](LICENSE)
