# Handwritten-Recognition-Using-MNIST
This project is all about the hand recognition of digit using keras 
next things is to shape the data differently, since we're treating the data as 2D images of 28 X 28 pixels instead of a flattened stream of 784 pixels. we need to shape it accordingly Depending on the data format keras is set up for this may be 1 x 28 x 28 or 28 x 28 x 1 the 1's indicates a single color channel as this is just grayscale if we were dealing with color images it would be 3 instead of 1 since we'd have red green and blue color channels)



For the meat of the problem. setting up a convolutional neural network involues more layers. Not all of these are strickly necessary, we could run the cell without pooling and dropout, but those extra steps help avoid overfitting and help things run faster

we'll start with a 2D convolution of the image-it's set up to take 32 windows, or "filters", of each image, each filter being 3 X 3 in size

we then run a second convolution on top of that with 64 3X3 windows-this topology is just what comes recommended with keras's own examples. Again we want to re-use previous research whenever possible while tuning CNN's as it is hard to do

Next we apply a Maxpooling2D layer that takes the maximum of each 2X2 result to distill the results down into something more manageable

A dropout filter is then applied to prevent overfitting


