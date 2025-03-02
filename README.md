## Kubernetes Deployment for Microservices
# Overview
- This repo consists Kubernetes deployment files to create namespace, pull image, and to create service for below three microservices.
    - [Python-Fast-APIs](https://github.com/adarshkoppamanjunath/Python-Fast-APIs)
    - [Python-Streamlit](https://github.com/adarshkoppamanjunath/Python-Streamlit)
    - [Robotframework-Tests](https://github.com/adarshkoppamanjunath/RobotFramework-Selenium-Requests)

# To use this locally,
- Install docker and minikube.
- Kubectl deploy -f namespace.yaml
- kubectl deploy -f Python-Fast-APIs\fastapi-deployment.yaml
- kubectl deploy -f Python-Fast-APIs\fastapi-service-internal.yaml
- kubectl deploy -f Python-Streamlit\streamlit-deployment.yaml
- kubectl deploy -f Python-Streamlit\streamlit-service.yaml
- kubectl deploy -f Robotframework-Tests\robotframework-deployment.yaml
- kubectl port-forward service/pythonstreamlit-service-internal 8501:80 -n fastapi-namespace

# How it works?
- [Python-Fast-APIs](https://github.com/adarshkoppamanjunath/Python-Fast-APIs)- microservice consists all backend apis inlcuding token and CRUD APIs.
- [Python-Streamlit](https://github.com/adarshkoppamanjunath/Python-Streamlit)- microservice include frontend which uses backend [Python-Fast-APIs](https://github.com/adarshkoppamanjunath/Python-Fast-APIs)
- [Robotframework-Tests](https://github.com/adarshkoppamanjunath/RobotFramework-Selenium-Requests)-microservice has API tests which whill talk to Pyhon-Fast-APIs
- LogIn to `http://localhost:8501/` with username `testuser` and password `secret`




