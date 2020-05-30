# Project_mlops
# Project Description :
1. Create container image that’s has Python3 and Keras or Sklearn installed using dockerfile
2. When we launch this image, it should automatically starts train the model in the container.
3. Create a job chain of job1, job2, job3, job4 and job5 using build pipeline plugin in Jenkins
4. Job1 : Pull the Github repo automatically when some developers push repo to Github.
5. Job2 : By looking at the code or program file, Jenkins should automatically start the respective machine learning software installed 6. 6. interpreter install image container to deploy code and start training( eg. If code uses CNN, then Jenkins should start the container that has already installed all the softwares required for the cnn processing).
7. Job3 : Train your model and predict accuracy or metrics.
8. Job4 : if metrics accuracy is less than 80% , then tweak the machine learning model architecture.
9. Job5: Retrain the model or notify that the best model is being created
10. Create One extra job job6 for monitor : If container where app is running. fails due to any reason then this job should automatically 11. start the container again from where the last trained model left

# About ML Model :
I have created a model that predicts whether the image given is cat or dog. It is based on deep learning. I have created input layers, pooling layers, output layer, etc. Model uses folloeing libraries:
1. Keras
2. numpy

code asks to set the hyperparameter and then gives the result with some accuracy.
Link for code : https://github.com/New-Byte/mlops_code

# About Devops technologies:
I have used devops to achieve complete automation in Machine learning.
technologies used :
1. Docker (Container)
2. Jenkins (Pipeline)

# Integration of ML and Devops :
 As task demands, i have tried to achieve the complete automation using devops. It inclues :
 ## 1. Creating the environment automatically using docker : 
 Job of jenkins checks for libraries and automatically launches the OS accordingly, Creating the environment to run ML code.
 
 ## 2. Downloading the code from git :
  Job of jenkins downloads the code from github whenever developer changes it.
  
## 3. Running the code and checking accuracy :
 Another job automatically runs the code and checks the accuracy when triggered. If accuracy is less than 80 % tthe job automatically twikes the ML code and try to increase the accuracy. So, ML model possessess optimal accuracy.

# Pipeline :
 Jobs are triggered and build depending on success of previous job automatically Using the pipeline.
