# mlOps08

Workflows
Update config.yaml
Update secrets.yaml [Optional]
Update params.yaml
Update the entity
Update the configuration manager in src config
Update the components
Update the pipeline
Update the main.py
Update the dvc.yaml


MLFLOW_TRACKING_URI=https://dagshub.com/SHIVRAJSHINDE/mlOps08.mlflow \
MLFLOW_TRACKING_USERNAME=SHIVRAJSHINDE \
MLFLOW_TRACKING_PASSWORD=5499747c80911cda6c320b403a03d246f2295149 \
python script.py


export MLFLOW_TRACKING_URI=https://dagshub.com/SHIVRAJSHINDE/mlOps08.mlflow
export MLFLOW_TRACKING_USERNAME=SHIVRAJSHINDE 
export MLFLOW_TRACKING_PASSWORD=5499747c80911cda6c320b403a03d246f2295149

AWS-CICD-Deployment-with-Github-Actions
1. Login to AWS console.
2. Create IAM user for deployment
#with specific access

1. EC2 access : It is virtual machine

2. ECR: Elastic Container registry to save your docker image in aws


#Description: About the deployment

1. Build docker image of the source code

2. Push your docker image to ECR

3. Launch Your EC2 

4. Pull Your image from ECR in EC2

5. Lauch your docker image in EC2

#Policy:

1. AmazonEC2ContainerRegistryFullAccess

2. AmazonEC2FullAccess

3. Create ECR repo to store/save docker image
- Save the URI: 566373416292.dkr.ecr.us-east-1.amazonaws.com/chicken

4. Create EC2 machine (Ubuntu)

5. Open EC2 and Install docker in EC2 Machine:
#optinal
sudo apt-get update -y
sudo apt-get upgrade
#required
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo usermod -aG docker ubuntu
newgrp docker


6. Configure EC2 as self-hosted runner:--
setting>actions>runner>new self hosted runner> choose os> then run command one by one


7. Setup github secrets:
AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=
AWS_REGION = us-east-1
AWS_ECR_LOGIN_URI = 905418096737.dkr.ecr.eu-north-1.amazonaws.com
ECR_REPOSITORY_NAME = kidney

