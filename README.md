# Book-cover-generation
Link to open in Google Collab: https://clck.ru/32B38d

The aim of the study was to develop a neural network-based method for creating book covers. 

By using suggested way of cover design one can save money and make a process much faster and easier to control and manipulate compared to traditional methods.

Training set: WikiArt

A book cover examples, which have been achieved by using modified, based on developed method, GAN model. 

<img src="https://user-images.githubusercontent.com/92825775/192692494-07d1910e-e5e7-457d-bbbb-f10400d7f16a.png" width="400">

<img src="https://user-images.githubusercontent.com/92825775/192692964-a5cffe46-9aa3-4684-af01-308425d794eb.png" width="400">

## Used model
For the implementation of the project the model of the generative-adversarial network VQGAN + CLIP has been chosen. Used model is developed and published by Katherine Crowson.

## The main core of suggested method 
To use neural networks for generating raster and vector image of a book cover, to make module for adding book cover text elements and to demonstrate the result by using augmented reality technology.

## Network configuration
In order to achieve raster and vector images generation there was manual configuration of chosen model. After numerous experiments it can be concluded that with an increase in weight decay, the image becomes more detailed, but "loses" to lower values in the generation speed. 
Model produces raster type images when weight decay equals to 1.0е-6, meanwhile when weight decay equals to 0 or 1.0е-8 vector type ones are being achieved.

<img src="https://user-images.githubusercontent.com/92825775/192689837-0f0b77fe-a3a6-4506-b6fe-ade6fdbb5ed1.png" width="350">

Results of experiments with step size show that this parameter affects the appearance of new image elements. Based on the fact that with the step size equals to 0.1 the image is more suitable for the entered description, a decision was made to use it.

## Text elements implementation
This modification was necessary to add book cover text elements to the image.
The result of the modification is a program code with an implemented interface. User has the option to enter the title of the book, font size, color, etc.

![image](https://user-images.githubusercontent.com/92825775/192689632-58ff2a42-15eb-42a7-a878-3d3d3b094fb5.png)

## Cover demonstration using AR
Unity and Vuforia were chosen as the development tools for this module. It is not presented in current repository.

<img src="https://user-images.githubusercontent.com/92825775/192691503-c81eb228-35da-4149-b384-84ae1656156d.gif" width="350">

## Web architecture
For the future web release the following architecture has been developed.

<img src="https://user-images.githubusercontent.com/92825775/192690471-501c7404-e34b-4f91-9738-e6f93070a98b.png" width="550">

As well as database model.

<img src="https://user-images.githubusercontent.com/92825775/192690649-85a9d25a-8a8a-4924-8acb-d97efe17c180.png" width="500">

There also has been made UI design by using Figma. 

<img src="https://user-images.githubusercontent.com/92825775/192692105-07486c75-31d3-4747-a8a5-b1c28f3e4c83.png" width="500">
<img src="https://user-images.githubusercontent.com/92825775/192692170-a1dd1f62-c414-4049-87d8-5c718a65cd51.png" width="500">








