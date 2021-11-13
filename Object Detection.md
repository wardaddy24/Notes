https://blog.paperspace.com/train-yolov5-custom-data/
https://youtu.be/hTCmL3S4Obw
https://arxiv.org/pdf/1506.02640.pdf


Total layers = 26
Conv layers = 24
FC layers = 2

YOLO:
* YOLO frame object detection as a regression problem to spatially separated bounding boxes and associated class probabilities.

DPM:
* A single neural network predicts bounding boxes and class probabilities directly from full images in one evaluation. 
Systems like deformable parts models (DPM) use a sliding window approach where the classifier is run at evenly spaced locations
over the entire image.

R-CNN :
* R-CNN use region proposal methods to first generate potential bounding boxes in an image and then run a classifier on these proposed boxes.
After classification, post-processing is used to refine the bounding boxes, eliminate duplicate detections, and rescore the boxes based on
other objects in the scene. These complex pipelines are slow and hard to optimize because each individual component must be trained separately.

Advantages of YOLO:
* YOLO is extremely fast.
