# project3 - Image Classification using AWS sagemaker
This is the third project in the AWS machine learning nanodegree program. AWS sagemaker was used to fine-tune the ResNet18 pretained model on the dog breed dataset available in 
https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip
The project was completed by making good use of the tools available to a machine learning engineer. Among such tools are the Pytorch framework, a pretrained model, profiler,
debugger, together with the model to train and deploy an endpoint. The python scripts used as entry_points for the estimators are as follows respectively: hpo.py, train_model.py and inference.py, these are also present in the folder. The Functional API in PyTorch is used to create the network with the ResNet18 retrained model

hpo.py script was used for hperparameter tuning after which the best sets of hypermaters were used in training

train_model.py script was used to perform model profiling and debugging. The hook function required for debugging was stated

reference.py script used as entry point for model deployment makes it possible for data(image) to be passed to the endpoint for testing

# project pipeline
data preparations:
the notebook environment is prepared by installing all the required dependencies, the dataset is downloaded, unziped and loaded to S3
Training:
# Hyperparamter tuning
 For this experiment, I used ResNet18 model. Among other pre-trained models, ResNet(18) model is popularly used. It provides a fair balance between the model accuracy to the number of operations needed to excecute. Though ResNet18 model might tend to have a lower accuracy, It is comparably faster to train with than ResNet 50
 **completed training job**
 ![image](https://user-images.githubusercontent.com/94250309/150440158-12c2067a-9c5f-4b14-9d36-6d366fdd9a48.png)

**Logs metrics during the training process**
![image](https://user-images.githubusercontent.com/94250309/150440788-31f251e5-b70e-4ae8-8bd7-467b6413c444.png)

**Retrieve the best best hyperparameters from all your training jobs**
![image](https://user-images.githubusercontent.com/94250309/150441120-370723b7-e3ed-49fc-b5fa-879f90f4bd51.png)
two hyperparameters were tuned which are batch size and learning rate

## Debugging and Profiling
The training performance is checked by sagemaker debugger
During your training job, the Dataloader rule was the most frequently triggered
model loss ought to decrease

### Results
![image](https://user-images.githubusercontent.com/94250309/150447690-6267d9db-f71d-425a-87d1-1d2b8f852c22.png)

the CrossEntropyLoss_output tend to decrease during training which is good, no over fitting recorded


The profiler html file is provided among the files in this repository, for more information

## Model Deployment
After successfully conducing a training job with the best hyperparameter available, I easily called for deployment with pytorch_model.deploy(). I also run a prediction on the endpoint. the result was seen by opening the payload image as seen in the train and deploy notebook above

unfortunately, I hurriedly deleted the endpoint, (I honestly did not know I was supposed to take screenshots since it was not stated in the project steps in the classroom, I found out, after completing the task in my notebook when I opened the readme file) in order not to incure cost

