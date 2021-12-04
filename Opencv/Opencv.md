#### cv.split()
#### cv.merge()
#### cv.copyMakeBorder()
**Note** \
There is a difference between OpenCV addition and Numpy addition. OpenCV addition is a saturated operation while Numpy addition is a modulo operation.
#### cv.add() 
Image Addition
#### cv.addWeighted()
Image blending \

bitwise operations for putting one image over other.

cv.getTickCount() - returns the number of clock-cycles after a reference event
cv.getTickFrequency()
cv.useOptimized()
cv.setUseOptimized() 

Python scalar operations are faster than Numpy scalar operations.
So for operations including one or two elements, Python scalar is better than Numpy arrays. Numpy has the advantage when the size of the array is a little bit bigger.
 cv.countNonZero()  - src 	single-channel array.
