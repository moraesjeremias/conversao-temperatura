# Temperature Conversion API

## Create a Kubernetes Cluster with K3D

```sh
k3d cluster create -p "8082:30000@agent[0]" -a 1 --agents-memory "1g" -s 1 --servers-memory "1g"
```

## Install Wheight API in a K8s cluster with helm

```sh
helm upgrade --install --atomic --timeout 3m temp-api ./helm/temp-api -f ./helm/temp-api/values.yaml --set image.tag=<DOCKER_IMAGE_TAG_HASH>
```
