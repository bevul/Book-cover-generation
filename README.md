# Book-cover-generation
Link to open in Google Collab: https://clck.ru/32B38d

The aim of the study was to develop a neural network-based method for creating book covers. 

By using suggested way of cover design one can save money and make a process much faster and easier to control and manipulate compared to traditional methods.

Training set: WikiArt

## Used model
For the implementation of the project, the model of the generative-adversarial network VQGAN + CLIP was chosen. Used model developed and published by Katherine Crowson.

## The main core of suggested method 
To use neural networks for generating raster and vector image of a book cover, to apply modules for adding its text elements and to demonstrate the result using augmented reality technology.

## Network configuration
In order to achieve raster and vector images generation there was manual configuration of networks. After numerous experiments it can be concluded that with an increase in weight decay, the image becomes more detailed, but "loses" to lower values in the speed of formation of the finished image. 
Model produces raster type images when weight decay equals to 1.0е-6, meanwhile when weight decay equals to 0 or 1.0е-8 vector type ones are being achieved.

![image](https://user-images.githubusercontent.com/92825775/192689837-0f0b77fe-a3a6-4506-b6fe-ade6fdbb5ed1.png)


Results of experiments with step size show that this parameter affects the appearance of new image elements. Based on the fact that with the step size equals to 0.1 the image is more suitable for the entered description, a decision was made to use it.

## Text elements implementation
This modification was necessary to add cover text elements to the image.
The result of the modification is a program code with an implemented interface. The user has the option to enter the title of the book, font size, color, etc.

![image](https://user-images.githubusercontent.com/92825775/192689632-58ff2a42-15eb-42a7-a878-3d3d3b094fb5.png)


## Web architecture
