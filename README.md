# Generation of simple adversarial images

This was done on the MNIST dataset using an architecture defined by Michael Nielson (obtains 96% test accuracy without pooling/convolution layers or advanced activations)

![alt_text](/output_images/Nontargeted_4.png)

**Non-targeted adversarial image with targeted label 4 but is predicted as 2**

Non-targeted images were obtained by initially generating a random uniform array equivalent to the image size, and then performing forward/backpropagation on the generated image and then performing gradient descent to minimize the difference between the targeted label and currently predicted label.

![alt_text](/output_images/Targeted_4.png)

**Non-targeted adversarial image with targeted label 4, but is predicted as 9**

Targeted images are obtained by minimizing the difference between the adversarial image generated with a sample image in the dataset (with the required class) in addition to that done above. This means that this method needs access and knowledge of how the classifier/dataset works. 
