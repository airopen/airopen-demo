# AI with R on OpenShift

This repository contains the code and assets to reproduce the AIROPEN (AI with R on OpenShift) demo.

# Install & configure for app demo

Install RHOAI

Create project "minio"
Deploy minio by applying minio.yaml in a namespace "minio"

Create project "airopen"
Apply airopen-project.yaml in namespace airopen

[not needed for app: Apply workbench-images.yaml (namespace is explicitely set in yaml file)]

Apply mlserver.yaml (namespace is explicitely set in yaml file)

Create multi-model server (namespace airopen, create route, no token) and then a model based on xgboost-1 with bucket breastcancer-bucket and path models/1/test-model.bst. ==> TODO Automate this.

Apply shiny-app-template.yaml in airopen.

Create app in DevMode via "All services" (adapt APP_GIT_URI and MODEL_INFERENCE_URL).
