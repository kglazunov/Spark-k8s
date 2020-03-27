# This is for testing and education purpose only.
#### Example CI/CD pipeline with Spark cluster running in the docker.

Versions:
- SPARK_VERSION=2.4.3
- SCALA_VERSION=2.12.4
- HADOOP_VERSION=2.7

0) Create Jenkins docker container with needed plugins 
  `docker build -t "jenkins:custom" -f Dockerfile .`
1) Create a task for clone repo, creating containers and executing Pi.py in the Spark cluster 

From attached Jenkinsfile will be doing:
* Build Spark images with python36 and pyspark, numpy packages
* Run Spark cluster via docker-compose
* Run testing python script (Pi Estimation)
* Shutdown Spark cluster via docker-compose
* Remove Spark docker images

Spark images based on CentOS 7 with extra packages for debugging. Make sense to change it for something lightweight for example Alpine in case of every day running.

test 777
