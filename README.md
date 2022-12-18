# To build image

`npm run build:docker:hosting`

# To push the built image to the hub

`cd hosting && npm run push:docker`

# To run the built image

(be sure not to have conflicting processes on port 80)

`docker run -m 256m --cpus="2" -e PORT=80 -p 80:80 foxt451/devops`

or

`docker run -m 256m --cpus="2" -e PORT=80 -p 80:80 docker-labs-hosting`

# To run app locally

`cd hosting && npm start`

# K8S

1. `kubectl apply -f k8s/`
2. `minikube service helloworld --url`
