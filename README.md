##
AI-Based Sudoku solver by Backtracking Algorithm
#
Before running the application, know that you can set the modeltype variable in Run.py to either "CNN" or "KNN" to choose the Convolutional Neural Network or the K Nearest Neighbours Algorithm for Recognition. By default it is set to "KNN" 


The GUI Homepage that opens up as soon as you run the application.


You need to select an image of a Sudoku Puzzle through the GUI Home Page.

Once you press Next, a number of stages of image processing take place which are displayed by the GUI leading up to recognition. Here are snapshots of two of the stages:

For recognition, a CNN or KNN can be used. This option can be toggled as mentioned in the first point. Once recognized, the board is displayed and you can rectify any wrongly recognized entries in the board.

Finally click on reveal solution to display the solution.

#
Gaussian Blurring Blurring using a Gaussian function. This is to reduce noise and detail.

Adaptive Gaussian Thresholding Adaptive thresholding with a Gaussian Function to account for different illuminations in different parts of the image.

Slicing the grid into 81 slices to get images of each cell of the Sudoku board.

##
CNN Technique -
Layers A Convolution Layer, a Max Pooling layer flattened into a hidden layer followed by some Dropout Regularization, another hidden layer and finally the output layer. Each of the inner layer uses ReLu while the output layer uses softmax.
Compilation Adam optimizer and sparse categorical cross entropy loss.
Training The model is trained on the MNIST handwritten digits dataset which has around 70,000 28X28 images.
Accuracy Around 98 percent accuracy on the test set.
##
KNN Technique -
K value used is 3.
Training Trained on the MNIST handwritten digits dataset which has around 70,000 28X28 images.
Accuracy Around 97 percent accuracy on the test set.
