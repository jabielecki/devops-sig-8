This document showcases how to get started with Skaffold using [Docker](https://www.docker.com/)
and Kubernetes command-line tool, [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/).

## Before you begin

* [Install Docker](https://www.docker.com/get-started)
* [Install kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
* Configure `kubectl` to connect to a Kubernetes cluster. You can use
    * any Kubernetes platform with Skaffold; see [Picking the Right Solution](https://kubernetes.io/docs/setup/pick-right-solution/)
    from Kubernetes documentation for instructions on choosing the
    right platform.
    * [Google Kubernetes Engine](https://cloud.google.com/kubernetes-engine/)
    is a hosted Kubernetes solution. To set up `kubectl` with Google Kubernetes Engine,
    see [Kubernetes Engine Quickstart](https://cloud.google.com/kubernetes-engine/docs/quickstart).
    * [Minikube](https://kubernetes.io/docs/setup/minikube/) is
    a local Kubernetes solution best for development and testing. To set up
    `kubectl` with Minikube, see [Installing Minikube](https://kubernetes.io/docs/tasks/tools/install-minikube/).</p>

{{< alert title="Note" >}}
If you use a non-local solution, your Docker client needs to be configured
to push Docker images to an external Docker image registry. For setting up
Docker with Google Container Registry, see <a href=https://cloud.google.com/container-registry/docs/quickstart>Google Container Registry Quickstart</a>.
{{< /alert >}}

## Installing Skaffold

{{% tabs %}}
{{% tab "LINUX" %}}
### Stable binary

```bash
curl -Lo skaffold https://storage.googleapis.com/skaffold/releases/latest/skaffold-linux-amd64
chmod +x skaffold
sudo mv skaffold /usr/local/bin
```

### Latest bleeding edge binary

The latest **bleeding edge** build works as well.

```bash
curl -Lo skaffold https://storage.googleapis.com/skaffold/builds/latest/skaffold-linux-amd64
chmod +x skaffold
sudo mv skaffold /usr/local/bin
```

## Login to your registry
`docker login`

## Deploy
Use `skaffold run` to build and deploy your app once, on demand.

