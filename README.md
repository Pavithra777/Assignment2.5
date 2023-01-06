# Assignment2.5

We are getting following two inputs
    1. Image from MNIST dataset having handwritten number from 0 to 9
    2. Random number 0 to 9
There are two output from neural network
    1. Number refered in the MNIST image
    2. Sum of Number refered in the MNIST image and the random number
    
The objective is to create a neural network that predicts the handwritten numbers from the given image and also to predict its sum with a given random number  

Dataset Preparation
 1. Loaded dataset from MNIST
 2. MNISTWithExtraInput class will take a random number (say 5) and merge MNIST dataset with the random number.
 3. For 10 random number 0 to 9, we will have 10 MNISTWithExtraInput object. So each image will have 0 to 9 random numbers.
 4. Using CombineDataset class will merge the 10 MNISTWithExtraInput as 1 dataset. Totally will 600000 (60000*10)  data in the dataset.
 
 Neural network
  1. Predicts the handwritten numbers from the given image and also predict its sum with a given random number
  2. First input layer is the image and the first output layer is the number represented in the image.
  3. Here first output layer is concatenated with second input which is the random number.
  4. The final output layer gives the sum of number in the image and the random number.
  5. Second label is prepared by adding first label tensor with random number. 
  6. Here Cross-entropy loss Function is used.It measures the difference between the predicted probability distribution and the true probability distribution of the      classes.
  
  Training Logs
  
    epoch :  1 total loss :  10401.4091796875  correct1 :  595649 correct2 :  372379
    epoch :  2 total loss :  5014.6826171875  correct1 :  599665 correct2 :  501401
    epoch :  3 total loss :  3386.888427734375  correct1 :  599936 correct2 :  533625
    epoch :  4 total loss :  2402.40478515625  correct1 :  599984 correct2 :  552877
    epoch :  5 total loss :  1811.1605224609375  correct1 :  599994 correct2 :  564475

