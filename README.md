
![Tensorflow_logo](https://github.com/user-attachments/assets/426bc899-ce7b-4cc6-8c71-ca07cc446da3)

# NeuralNetworkRegression.tf
regression problems

## here we go here we introduce the regression problems  with neural networrks:
# what is a regression problem? 
A regression problem is a common type of supervised learning problem in Machine Learning. The end goal is to predict quantitative values – for example, continuous values such as the price of a car, the weight of a dog, and so on.


## one og the most important thing to do  understand better our is going our work with data is to visualize
one of the most popular libraries is called Mathplot  used  to show the behave of ours model, data ,and predictions. 
![Screenshot 2024-08-08 105203](https://github.com/user-attachments/assets/e7e4541d-306c-4ad1-8503-6f39885c00a2)
this is a good exaple of regression data.

# here we go our first model of course is not the best model in the planet but we will see how to improve this...
![Screenshot 2024-08-08 105453](https://github.com/user-attachments/assets/38bafff0-db6e-4f62-b262-e76ed38fe418)
#different way and things to check to improve our model.
![Screenshot 2024-08-08 105644](https://github.com/user-attachments/assets/a0e944b1-a63e-4825-81b2-3b18dc0a199b)

# how we can see in thits case how our model perform, we can see the chages:
* we add more hidden layers
* change the  optimizer from MAE to Adam()  we can add a learnin reate to specify  the learning time for our model during the process.
* the learning rate inside the optimizer

![Screenshot 2024-08-08 110250](https://github.com/user-attachments/assets/bddde465-c61e-4efc-b37b-fcf10b9760ad)
![Screenshot 2024-08-08 110307](https://github.com/user-attachments/assets/7cd89da0-34d8-43e9-91a5-db7273ee8c3d)
we can see the difference of performance between the first model and the second one
# but what is a MAE optimizer and the Adam ?  
### MAE takes the average of absolute errors for a group of predictions and observations as a measurement of the magnitude of errors for the entire group.
### is an iterative optimization algorithm used to minimize the loss function during the training of neural networks Adam can be looked at as a combination of RMSprop and Stochastic Gradient Descent with momentum.

# here for example we create other data to try another example and we try to divide ths data in training datat and testing data that is a very importat step for our model nrmally use the 80% in training data and the last 20 % is our test data.

![Screenshot 2024-08-08 111240](https://github.com/user-attachments/assets/2a3c37f3-586c-48bc-8f87-77c3dd7ec90e)

## here again other models
![Screenshot 2024-08-08 111641](https://github.com/user-attachments/assets/c11dd51a-e7c7-4b15-a994-de775173e41f)

# the function to plot this..
![Screenshot 2024-08-08 111830](https://github.com/user-attachments/assets/9c7181ac-657f-46dd-879e-95edcb89bf6d)

# and the graphic of this 
![Screenshot 2024-08-08 111852](https://github.com/user-attachments/assets/ddbeee9a-ada2-4ea9-83b5-27c1bc741b0e)

 ### in this series of info i will not put all the model  i will just show the graphics to let you understand how the performe and the changement i made in the model to have this result 
the most of the time this models  we will change the optimizers to have a better performance  and the learning_rate of this to understand  test...


 ## this two  function are to see the result of the mean in little and big scale  to simplify mae:little_scale mse:big_scale 
 def mae(y_true, y_pred):
    return tf.keras.metrics.mean_absolute_error(y_true, y_pred).numpy()

def mse(y_true, y_pred):
    return tf.keras.metrics.mean_squared_error(y_true, y_pred).numpy()

mae_1 = mae(y_true=y_test, y_pred=y_preds_1)
mse_1 = mse(y_true=y_test, y_pred=y_preds_1)
print(f'MAE: {mae_1}, MSE: {mse_1}')


# here we ho we can admire after few test the perfect model that fit perfectly our test data 
![Screenshot 2024-08-08 112939](https://github.com/user-attachments/assets/499c6e35-34fa-40e6-9b42-e85e4c7fcfd5)

## we can see in this example how  the red dots fit in a perfect way so we receive a perfect prediction on out testinf data

![Screenshot 2024-08-08 113622](https://github.com/user-attachments/assets/687e0b5b-6e3a-4e17-bcc5-95b09b9a0b5d)

### and here we go: 
![vae](https://github.com/user-attachments/assets/51b5d224-41af-46ac-8a59-195da560a9cc)

we sow a lot till now and we will see more soon! 

## this last part is dedicated to the saving our perfect model and load this thig very very simple!




