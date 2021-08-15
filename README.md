# Deploying containerized applications to Amazon ECS using AWS CodePipeline, AWS CodeBuild, Amazon ECR, and AWS CloudFormation

# Solution Architecture Overview:

For the purpose of isolating application source code changes from any Infrastructure changes, I created 2 branches that are responsible for 2 different pipelines as following:

   1- infrastructure branch: holds the infrastructure pipeline cloudformation template, and all related resources templates that are used to build the ECS Fargate Cluster where the application will be deployed.
    
   2- Main branch: holds the Application pipeline cloudformation template that is used to build the source code, push a ready docker image to AWS ECR, deploy it to Beta environment (Test Env), test it, manually approve deploying to Alfa environment (Production Env), and finally deploy to Alfa environment.
   
# Infrastructure Pipeline HLD:
 
![alt text](https://github.com/Ahmedmagddi/aws-ecs-fargate/blob/main/images/infra%20pipeline%20hld.png?raw=true)

# After Executing infrastructure pipeline stack:

![alt text](https://github.com/Ahmedmagddi/aws-ecs-fargate/blob/main/images/INFRA-PIPELINE.png?raw=true)

# Application Pipeline HLD:

![alt text](https://github.com/Ahmedmagddi/aws-ecs-fargate/blob/main/images/Application%20pipeline%20hld.png?raw=true)

# After Executing Application pipeline stack:

![alt text](https://github.com/Ahmedmagddi/aws-ecs-fargate/blob/main/images/APP-PIPELINE01.png?raw=true)

![alt text](https://github.com/Ahmedmagddi/aws-ecs-fargate/blob/main/images/APP-PIPELINE02.png?raw=true)
