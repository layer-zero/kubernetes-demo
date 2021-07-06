# Kubernetes demo

I created this demo while studying for the Cisco DEVCOR course. It contains the necessary files to deploy an application consisting of a simple web frontend and database backend to play with on my local Kubernetes cluster.

Also note that this demo was created using the Docker Desktop for Mac built-in Kubernetes cluster. To make this work on other Kubernetes deployments it will require some modifications. (For example, I am using the local Docker repository for the images and using a local directory as a volume for the database server, which will not work on other types of Kubernetes clusters without making appropriate modifications).

First, build the local docker image using `./build`.<br>
Then use `./run` to deploy the containers, create a service, and create an ingress.

\(An nginx ingress controller has already been created using the command
`kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v0.47.0/deploy/static/provider/cloud/deploy.yaml` as described in the [installation guide](https://kubernetes.github.io/ingress-nginx/deploy/#docker-for-mac)\)

Test by pointing your browser to http://localhost/devcor-app or http://kubernetes.docker.internal/devcor-app.<br>
You should see the welcome page and refreshing should cycle through the local IP addresses of the pod.

Use `./stop` to remove the containers, service, and ingress.<br>
Finally, use `./clean` to remove the container image.
