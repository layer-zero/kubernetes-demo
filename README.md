# Kubernetes demo

First, build the local docker image using `./build`.<br>
Then use `./run` to deploy the containers, create a service, and create an ingress.

\(An nginx ingress controller has already been created using the command
`kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v0.47.0/deploy/static/provider/cloud/deploy.yaml` as described in the [installation guide](https://kubernetes.github.io/ingress-nginx/deploy/#docker-for-mac)\)

Test by pointing your browser to http://localhost/devcor-app or http://kubernetes.docker.internal/devcor-app.<br>
You should see the welcome page and refreshing should cycle through the local IP addresses of the pod.

Use `./stop` to remove the containers, service, and ingress.<br>
Finally, use `./clean` to remove the container image.
