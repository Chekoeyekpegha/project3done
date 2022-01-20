# project3 - Image Classification using AWS sagemaker
This is the third project in the AWS machine learning nanodegree program. AWS sagemaker was used to fine-tune the ResNet18 pretained model on the dog breed dataset available in 
https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip
The project was completed by making good use of the tools available to a machine learning engineer. Among such tools are the Pytorch framework, a pretrained model, profiler,
debugger, together with the model to train and deploy an endpoint.

# project pipeline
data preparations:
the notebook environment is prepared by installing all the required dependencies, the dataset is downloaded, unziped and loaded to S3
Training:
# Hyperparamter tuning
 For this experiment, I used ResNet18 model. Among other pre-trained models, ResNet(18) model is popularly used. It provides a fair balance between the model accuracy to the number of operations needed to excecute. Though ResNet18 model might tend to have a lower accuracy, It is comparably faster to train with than ResNet 50
 # completed training job
 ![image](https://user-images.githubusercontent.com/94250309/150440158-12c2067a-9c5f-4b14-9d36-6d366fdd9a48.png)

 # project pipeline
Deployment:i


Remember that your README should:
- Include a screenshot of completed training jobs
- Logs metrics during the training process
- Tune at least two hyperparameters
- Retrieve the best best hyperparameters from all your training jobs

## Debugging and Profiling
**TODO**: Give an overview of how you performed model debugging and profiling in Sagemaker

### Results
**TODO**: What are the results/insights did you get by profiling/debugging your model?

**TODO** Remember to provide the profiler html/pdf file in your submission.


## Model Deployment
**TODO**: Give an overview of the deployed model and instructions on how to query the endpoint with a sample input.

**TODO** Remember to provide a screenshot of the deployed active endpoint in Sagemaker.

## Standout Suggestions
**TODO (Optional):** This is where you can provide information about any standout suggestions that you have attempted.

