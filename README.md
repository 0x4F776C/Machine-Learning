# Machine-Learning
Repository to store my progress in Machine Learning field

## Steps to follow

1. [Let's go through some memes](https://medium.com/nybles/understanding-machine-learning-through-memes-4580b67527bf)

2. Docker container for Jupyter notebook
```console
# Grab Docker image from Jupyter Docker repository
docker pull jupyter/all-spark-notebook

# Start container - Windows
docker run -d -P --name jupyter-notebook -v D:\data-science:/home/jovyan/work jupyter/all-spark-notebook

# Start container - Linux
docker run -d -P --name jupyter-notebook -v ~/data-science:/home/jovyan/work jupyter/all-spark-notebook

# Obtain the random host port assigned to the container
docker port jupyter-notebook 8888

# Obtain Jupyter notebook token
docker logs --tail 3 jupyter-notebook
```

3. Access Jupyter notebook
```console
Open web browser

Go to "http://localhost:<random host port>?token=<token>"
Example: http://127.0.0.1:32773/?token=19625e70bd3f90a2bcd9519620a55ea3703bdede0a48d277
```
![Web UI](https://github.com/0x4F776C/Machine-Learning/blob/main/screenshots/jupyter-notebook.PNG)

4. Kill container
```console
# Stop container
docker stop jupyter-notebook

# Remove the container
docker rm jupyter-notebook
```
