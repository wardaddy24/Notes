[BLOG_YOLO_TRAINING](https://blog.paperspace.com/train-yolov5-custom-data/)
[YOUTUBE VIDEO FOR CUSTOM DATASET TRAINING](https://youtu.be/hTCmL3S4Obw)
[YOLO PAPER](https://arxiv.org/pdf/1506.02640.pdf)


Total layers = 26
Conv layers = 24
FC layers = 2

Our system models detection as a regression problem. It divides the image into an S × S grid and for each
grid cell predicts B bounding boxes, confidence for those boxes,and C class probabilities. These predictions are encoded
as an S × S × (B ∗ 5 + C) tensor.If the center of an object falls into a grid cell, that grid cell is responsible for detecting
that object.Each bounding box consists of 5 predictions: x, y, w, h,and confidence.
* The (x; y) coordinates represent the center of the box relative to the bounds of the grid cell. 
* The width and height are predicted relative to the whole image.
* Finally the confidence prediction represents the IOU between the predicted box and any ground truth box
* Each grid cell also predicts C conditional class probabilities,
Pr(ClassijObject). These probabilities are conditioned on the grid cell containing an object. We only predict
one set of class probabilities per grid cell, regardless of the number of boxes B.
At test time we multiply the conditional class probabilities and the individual box confidence predictions,
** Pr(ClassijObject)  Pr(Object)  IOUtruthpred = Pr(Classi)  IOUtruthpred ** 
which gives us class-specific confidence scores for each box. These scores encode both the probability of that class
appearing in the box and how well the predicted box fits the object.
### YOLO:
* YOLO frame object detection as a regression problem to spatially separated bounding boxes and associated class probabilities.

### DPM:
* A single neural network predicts bounding boxes and class probabilities directly from full images in one evaluation. 
Systems like deformable parts models (DPM) use a sliding window approach where the classifier is run at evenly spaced locations
over the entire image.

### R-CNN :
* R-CNN use region proposal methods to first generate potential bounding boxes in an image and then run a classifier on these proposed boxes.
After classification, post-processing is used to refine the bounding boxes, eliminate duplicate detections, and rescore the boxes based on
other objects in the scene. These complex pipelines are slow and hard to optimize because each individual component must be trained separately.

#### Advantages of YOLO:
* YOLO is extremely fast.
* YOLO reasons globally about the image when making predictions.
* YOLO learns generalizable representations of objects.(Performs better on artworks after traininf from natural images)

#### Disadvantages of YOLO:
* struggles with small objects that appear in groups, such as flocks of birds.
* incorrect localizations
