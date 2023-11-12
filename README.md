# nuralstyle

This code implements neural style transfer using a pre-trained VGG19 model in TensorFlow and Keras. Let's break down the code into different sections:

Importing Necessary Libraries:
The code starts by importing the required libraries, including TensorFlow, Keras, NumPy, PIL (Python Imaging Library), and Matplotlib.

Loading Images:
There are functions defined to load and preprocess content and style images. These functions use the PIL library to open images, resize them, and convert them to NumPy arrays.

Image Plotting:
A function is defined to plot images using Matplotlib.

Model Architecture:
The VGG19 model is imported from Keras applications, and its summary is displayed. The model is then used to create a custom model that extracts specific layers for content and style features.

Loss Functions:
Functions for content loss and style loss are defined. The style loss involves calculating the Gram matrix to capture the correlation between feature maps.

Feature Extraction:
A function is defined to extract content and style features from the given content and style images using the previously defined model.

Loss Computation:
A function computes the total loss, style loss, and content loss based on the extracted features.

Gradient Computation:
A function calculates the gradient of the total loss with respect to the input image.

Style Transfer Function:
The main function run_style_transfer orchestrates the style transfer process. It initializes the model, extracts features, defines optimization parameters, and iteratively updates the input image to minimize the total loss.

Style Transfer Visualization:
The final section visualizes the style transfer process by displaying images at different epochs during optimization. The best image and its associated loss are returned.

Style Transfer Results:
The code concludes with the visualization of the content image, style image, and the generated style transfer image.

Summary:
The overall purpose of the code is to perform neural style transfer using a VGG19 model. It defines functions for image processing, feature extraction, loss computation, and optimization. The visualization at each epoch provides insights into how the generated image evolves over time to combine the content of one image with the artistic style of another.
