# Scania-Truck-Failures
## Technologies : Machine Learning Technology
## Domain:  Transportation
## Problem Statement :
The Air Pressure System (APS) is a critical component of a heavy-duty vehicle thatuses compressed air to force a piston to provide pressure to the brake pads, slowing
the vehicle down. The benefits of using an APS instead of a hydraulic system are the
easy availability and long-term sustainability of natural air.
This is a Binary Classification problem, in which the affirmative class indicates that the
failure was caused by a certain component of the APS, while the negative class
indicates that the failure was caused by something else.

AIM : To reduce the cost due to unnecessary repairs. So it is required to minimize the false predictions.
---
## **Steps Involved**
* Step 1: created a python script to dump our data from local to mongodb
* Step 2: performed EDA, FeatureEngineering and Model building on JupyterNotebook and google colab
### Now, perform the step2 in modular programing way:
* step 3: created setup.py file for the distribution purpose of my source code
* step 4: created project file/folder structure
* step 5: implemented logger concepts
* step 6: implemented Custom exception concepts
* step 7: data_ingestion done
* step 8: data_validation done
* step 9: data_transformation done
* step 10: model_training done
* step 11: model_evaluation done
* step 12: model_pusher done
* step 13: created training pipeline
* step 14: created batch_prediction pipeline
## with the above following steps ML development part done. next we will move into deployment part on AWS cloud.
---
# Deployment Part
---
1. Login to AWS console.

2. Create IAM user for deployment

	with specific access
	1. EC2 access : It is virtual machine
	2. ECR: Elastic Container registry
  Policy:
	1. AmazonEC2ContainerRegistryFullAccess
	2. AmazonEC2FullAccess
	To save your docker image in aws

	Description: About the deployment:
	1. Build docker image of the source code
	2. Push your docker image to ECR
	3. Launch Your EC2 
	4. Pull Your image from ECR in EC2
	5. Lauch your docker image in EC2
	
3. Create ECR repo to store/save docker image
    - Save the URI: 
4. Create EC2 machine (Ubuntu) 
5. Open EC2 and Install docker in EC2 Machine:
	### optional
	1. sudo apt-get update -y
	2. sudo apt-get upgrade
	### required
	1. curl -fsSL https://get.docker.com -o get-docker.sh
	2. sudo sh get-docker.sh
	3. sudo usermod -aG docker ubuntu
	4. newgrp docker	
6. Configure EC2 as self-hosted runner:
   1. setting>actions>runner>new self hosted runner> choose os> 
   2. then run command one by one on ec2 cli
7. Setup github secrets:
   1. AWS_ACCESS_KEY_ID=
   2. AWS_SECRET_ACCESS_KEY=
   3. AWS_REGION = 
   4. AWS_ECR_LOGIN_URI = 
   5. ECR_REPOSITORY_NAME =
   6. S3 bucket name =
   7. MongoDB url :
    

