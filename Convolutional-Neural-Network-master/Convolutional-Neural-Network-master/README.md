# Convolutional-Neural-Network
#For better understanding of CNN please visit CNN/Wikipedia.
#Here I have performed classification on NSLKDD dataset avialable on github.

### Data preprocessing: The train++ and test21+ file from nslkdd dataset is being pre-processed before giving it to model. I have taken approach of converting data to 8 bit greyscale image. It is not necessary to convert the data to greyscale but CNN works better with images so I converted the data to 8bit greyscale images.

#steps of pre-processing:
1> The dataset comes in mixed format which has categorical, continous and binary values. We have to first normalize the data which  has value between 0 and 1.
2> For the categorical data, label encode the data with sklearn label encoder.
3> Now all the data is in numreical format, perform min-max normalization on the dataset.
4> Now we have 41 features, having value between 0 and 1. Next step is to one-hot encode all the 41 features in bin size of 10. Thats how we now have 410 dimesional dataset.
5> I performed variance threshold on the dataset and found 10 dimension with no dataset worthy of use. So I removed the dataset to 400 dim.
6> Reshape the data on each row in form of 50*8 matrix.
7> Now for every 8bit convert it to greyscale pixel. Now we have final dataset in form of 1 row 50 dimesion.

### Now you can apply the CNN model with shufflesplit on this dataset and can check accuracy.
