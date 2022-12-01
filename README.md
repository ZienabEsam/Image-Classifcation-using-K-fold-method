# Image-Classifcation-using-K-fold-method
Image classification using K fold method
Using the Flower recognition dataset on Kaggale as a test:

Applying K fold method on Images, I trained the model using AlexNet, optained a test accuracy 81 % and Train Accuracy 90 % 
You can get better results, by changing the model tray other transfer learning models like Xception net or DensNet or any pther image classification tansfer learning models.

The K fold method is relying on using the whole dataset to train the model , you can devide the Dataset into K folds in my case I used K equals 3,
 you can choose anotehr value depending on your dataset.
 
 After you devide the dataset into K "Not manual, just choose number of folds" .
 
 You will import your dataset normaly and devide it into X & Y, and of course do the preprocessing work.
 The most immportant  part is how to apply your k fold method:
 
 you will have to create a for loop to train your folds of data using the kf.split() method, but you have to define your model inside the loop so that the model create a randome set of images every time not the same split that it used in previous trained versions for the model to start fom scratch every time and take the average manually at the end.
 
 for train_index, test_index in kf.split(X) :
    X_train, X_test = X[train_index], X[test_index]
    y_train, y_test = y[train_index], y[test_index]
 
 
