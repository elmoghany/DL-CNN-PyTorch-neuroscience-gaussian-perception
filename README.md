# Objective
Identify the line if it is vertical or horizontal

# Illustration
1) Training: We train a CNN model on an input picture of a random gaussian noise with a horizontal and vertical bars as occlusion 
2) Accuracy: The model accuracy reached 99% 

# Model & Architecture
1) CNN DL Model
2) Image size 30x30 pixel
3) 3 convolution layers + batchnorm + leaky_relu
4) Linear layer + leaky_relu + dropout 0.5
5) inChans  = 1 # RGB
6) outChans = 64 # of feature maps / kernels
7) krnSize  = 3x3 # odd number
8) padding  = 0 # No padding
9) stride   = 1 # use stride instead of maxpool
10) batchnorm = 1
11) Use of BCEWithLogitsLoss (BCE with sigmoid) for classification of horizontal or vertical line

# Results
1) Note: The test images are not vertical nor horizontal but they have slope
2) Good Results: The model was able to identify well the components of the line slope whether if it is nearer to be horizontal or vertical
