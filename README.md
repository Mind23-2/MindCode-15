# [CenterNet Description](https://gitee.com/mindspore/models/blob/r1.6/research/cv/centernet/README.md#contents)

CenterNet is a novel practical anchor-free method for object detection, 3D detection, and pose estimation, which detect identifies objects as axis-aligned boxes in an image. The detector uses keypoint estimation to find center points and regresses to all other object properties, such as size, 3D location, orientation, and even pose. In nature, it's a one-stage method to simultaneously predict center location and bboxes with real-time speed and higher accuracy than corresponding bounding box based detectors. We support training and evaluation on Ascend910.

[Paper](https://gitee.com/link?target=https%3A%2F%2Farxiv.org%2Fpdf%2F1904.07850.pdf): Objects as Points. 2019. Xingyi Zhou(UT Austin) and Dequan Wang(UC Berkeley) and Philipp Krahenbuhl(UT Austin)

# [Model Architecture](https://gitee.com/mindspore/models/blob/r1.6/research/cv/centernet/README.md#contents)

In the current model, we use CenterNet to estimate multi-person pose. The DLA(Deep Layer Aggregation) net was adopted as backbone, a 3x3 convolutional layer with 256 channel was added before each output head, and a final 1x1 convolution then produced the desired output. Six losses are presented, and the total loss is their weighted mean.

[RepoLink](https://gitee.com/mindspore/models/tree/r1.6/research/cv/centernet)