# AmericanSignLanguage_Reader
Project Data: The Dataset is 1.11 GB in Size. The images in the dataset are manually captured  and not computer-generated. The dataset linked above contains images from 29 classes (26  alphabets, SPACE, DELETE, and NOTHING). Each class contains 3000 images in the training set  and each image is a 200 x 200 RGB image.  The training data set contains 87,000 images, of which 26 are for the letters A-Z and 3 classes for  SPACE, DELETE, and NOTHING.  These 3 classes are very helpful in real-time applications and classification.  The test data set contains a mere 29 images, to encourage the use of real-world test images.>the test  set is very small. We plan to Experiment with different architectures and  hyperparameters. First, implement the CNN architecture described in the Models of [8] and apply our  training data to generate the classification of 26 Letters. Our goal is to map images from a particular  domain to a Letter that it means. We will be finetuning (transfer learning) existing models that  perform classification on RGB images. We will Look at the levels of RGB images in Particular  Centroidal Pixels and We can Classify from the Centre Which Shape is Defined. We are Planing to  Use RESNET - Residual Neural Networks or Similar to be able to argue and analyze the better  Accuracy between all of the Networks. 


Results: 
We have achieved an Accuracy: 75.38850574712643 in our Single Layer model using only layer 1 of our algorithm , Accuracy : 52.79655172413793 with Using Weight Decay regularize in the same Model. 
Taking Model 2: 2 Layers CNN we got Accuracy: 55.880459770114946.

Using 3 Layer CNNs with proper Parameters, changed the low accuracy values and shoed us the best accuracies possible.
3 Layer CNNs: Accuracy: 99.32528735632184 with 3x3 kernel
And Accuracy: 94.41034482758621 with 5x5 kernel. -> which can be proven further as the receptive field of the 5x5 kernel can be covered by two 3x3 kernels.

Trying out the 5 Layer CNNs: Accuracy: 93.52068965517242 which was lower than 3 layered.
We found Accuracies which are a better accuracy then most of the current research papers on American sign language. You can Look at the table below for results.

RESNET: Model 1 gave us: Accuracy: 96.24942528735633 Model 2 gave us Accuracy: 97.84137931034482 with SGD Optimizer.

Model	No. of Conv layers	kernel	Padding	Weight Decay	Dropout	Training Acc	Test Acc
CNN1_layer	1	5x5	2	no	0.2	75.38	-
CNN1_regular.	1	5x5	2	yes	0.2	52.79	-
CNN2_layers	2	5x5	2	yes	0.2	55.88	-
CNN3_layers	3	3x3	same	yes	0.2	99.32	-
CNN3_layers2	3	3x3	same	yes	0.5	99.25	-
CNN3_kernel5	3	5x5	same	yes	0.5	94.41	-
CNN5_layers	5	3x3	same	yes	0.5	93.52	78.57
RESNET_Adam	50	1x1, 3x3	-	no	yes	96.25	100
RESNET_SGD	50	yes	-	no	yes	97.84	100

