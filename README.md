# Hive and SparkSQL

### Getting started

#### How to run notebook for exercises
- Get container from dockerhub
  - `docker pull <container_name>` (Note: <container_name> for hive part of the course: `bigdatateam/hive-course2`)
- Start container
  - `docker run --rm -it -p 8888:8888 <container_name>`
- Visit notebook @ http://localhost:8888


#### How to run bash shell for experimentation
- Start bash process in container
  - docker run --rm -it -v `pwd`:/home/jovyan/sandbox -p 8888:8888 bigdatateam/hive-course2 bash
- Start hive interface
  - `\# hive`