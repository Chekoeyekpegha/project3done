# project3 - Image Classification using AWS sagemaker
This is the third project in the AWS machine learning nanodegree program. AWS sagemaker was used to fine-tune the ResNet18 pretained model on the dog breed dataset available in 
https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip
The project was completed by making good use of the tools available to a machine learning engineer. Among such tools are the Pytorch framework, a pretrained model, profiler,
debugger, together with the model to train and deploy an endpoint.

#project pipeline
data preparations:
the notebook environment is prepared by installing all the required dependencies, the dataset is downloaded, unziped and loaded to S3
Training:
#Hyperparameter tuning
 For this experiment, I used ResNet18 model. Among many other pre-trained models, ResNet(18) model is popularly used. It provides a fair balance between the model accuracy to the number of operations needed to excecute. Though ResNet18 model might tend to lower accuracy, It is comparably faster to train with than ResNet 50
Deployment:

