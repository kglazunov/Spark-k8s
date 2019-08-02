# This is for testing and education purpose only.
0) Create Jenkins docker container with needed plugins 
  `docker build -f Dockerfile .`
1) Create a task for clone repo, creating containers and executing Pi.py in the Spark cluster 
From attached Jenkinsfile will be doing:
* Build Spark images with python36 and pyspark, numpy packages
* Run Spark cluster via docker-compose
* Run testing python script (Pi Estimation)
* Shutdown Spark cluster via docker-compose
* Remove Spark docker images
