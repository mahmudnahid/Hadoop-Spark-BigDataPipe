# Stock Price Analysis using Big Data Tools & Techniques:

The goal of this project is to investigate the correlation between the stock price performance of Tesla and the sentiment of news surrounding the company. With the rapid growth of big data and advancements in AI technologies, it has become increasingly important to utilize these tools in analyzing large volumes of data to derive meaningful insights. By leveraging big data tools and techniques, we can identify patterns and trends in the relationship between stock prices and news sentiment.

# Architechture:

The project demonstartes how to create pipelines for big data from various sources like Hadoop, MongoDB, MySQL and process it with Spark. The layers of the system are explained in the following diagram:

![Architechture](./assets/1_architecture.png?raw=true "Architechture")

# Setup:

All the applications are dockerized and you can spin up the cluster by using the following commands:

```
#Create network
docker network create -d bridge bds-network

#Create hadoop base image
cd hadoop/base && docker build . -t hadoop-base && cd ../..

#Create spark base image
cd spark/base && docker build . -t spark-base && cd ../..

#Start all containers
docker-compose up -d

```

![Setup](./assets/2_docker_cluster.JPG?raw=true "Setup")

# Notebook:

After setting up the environment you can check the [Jupyter notebook](https://github.com/mahmudnahid/Hadoop-Spark-BigDataPipe/blob/main/jupyter/workspace/hadoop_spark_pipeline.ipynb) for running the pipe:

![Notebook](./assets/3_notebook.JPG?raw=true "Setup")



### Hadoop
Access Hadoop UI on ' http://localhost:9870 '

### Spark
Access Spark Master UI on ' http://localhost:8080 '

### Jupyter
Access Jupyter UI on ' http://localhost:8888 '
