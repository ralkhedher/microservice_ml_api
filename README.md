[![ralkhedher](https://circleci.com/gh/ralkhedher/microservice_ml_api.svg?style=svg)](https://app.circleci.com/pipelines/github/ralkhedher/microservice_ml_api)

# Introduction
## Machine Learning Microservice API
An implementation of a pre-trained machine learning model trained to predict the housing prices in Boston. The backend is powered by `Python` minimalistic framework `Flask`. It tests skills such as `Docker`, `Kubernetes`, `Python`, `Linux`, and `data science`. 
You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). pre-trained machine learning model, such as those for image recognition and data labeling.

## This project!

- Runs a docker container
- Upload container to *Docker Hub* a container registry.
- Run the deployed application in a Kubernetes cluster
- Makes House prices prediction
- Integrate with CircleCI for continuous integration

## Requirements
 - Python 3 +

## STEPS

### Step 0
- Clone the repo to your remote server environment
- Server specs
`Ubuntu 18.04 Server -> t3.small -> 2Gib 2Ram -> 20GB`
- Connect to the project using `vscode` _Remote Explorer_ extension forseamless workflow.

### Step 1: Install dependencies
- Create a virtual enviroment `python3 -m venv ~/.devops` and activate `source ~/.devops/bin/activate`
- Install dependencies by running `make install`. This install deps' stored in the `requirements.txt` file.

### Step 2: Run Docker container
- Run the application on docker by calling `./run_docker.sh`

### Step 3: Install Minikube
- Serves as a local k8s cluster. After install, 
- Start minikube `minikube start`

### Step 4: Upload to Docker Hub
- In the `./upload_docker.sh` add a docker path as specified.
- To upload to docker hub, run `./upload_docker.sh`

### Step 5: Kubernetes deployment
- To deploy to kubernetes, run `./run_kubernetes.sh`

### Step 6: Make Predictions
- After running `./run_kubernetes.sh` that spins up a pod.
- Open a new tab and run a prediction by executing `./make_prediction.sh`

### Step 7: Destroy Minikube
- Run ` minikube stop`