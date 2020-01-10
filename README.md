# Tensorflow 2.0 Advanced: Deep Dream Project 1.

# PROBLEM STATEMENT
 - Deep dream is a computer vision algorithm created by Alexander Mordvintsev from Google.
 - The algorithm works by creating dream-like effect. It’s like giving humans an extremely powerful drug!
 - When you feed in an image to a trained ANN, the neurons fire and generate activations. The deep dream algorithm work by trying to change the input image in a way that would make some of these neurons fire more (boost the neurons firing or activations).
 - You can select which neurons in which layer you are interested in making them fire more prominently.
 - The process is continuously repeated until the input image now contains all features that a specific layer was originally looking for.
 - Example: if a certain layer was expert in recognizing dog faces and you feed in an image of a blue sky, the deep dream algorithm will continuously change the input image and start creating images of dogs faces on top of the blue sky. The process keep repeating until the layer of interest is happy with the results!
### Deep Dream Steps:
 - Forward an image through a trained ANN, CNN, ResNet..etc
 - Select a layer of choice (first layers capture edges, deep layers capture full shapes such as faces)
 - Calculate the activations (output) coming out from the layer of interest.
 - Calculate the gradient of the activations with respect to the input image
 - Modify the image to increase these activations, and thus enhance the patterns seen by the network resulting in trippy hallucinated image!
 - Iterate and repeat over multiple scales
 
 #### With Deep Dream, this painting by Henri Matisse:
 ![alt text](https://github.com/johangenis/TF-2.0-Advanced-Deep-Dream-Project-1-AI-artist/blob/master/chatEtPoissonsRouge.jpg "Original Artwork")
 
 #### was transformed into this:
 ![alt text](https://github.com/johangenis/TF-2.0-Advanced-Deep-Dream-Project-1-AI-artist/blob/master/chatEtPoissonsRouge_DeepDreamAltered.png "Deep Dream Altered Artwork")
 
This code is adapted from Tensorflow 2.0 Documentation: https://www.tensorflow.org/beta/tutorials/generative/deepdream
