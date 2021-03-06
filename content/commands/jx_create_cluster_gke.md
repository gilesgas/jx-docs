---
date: 2018-09-17T16:50:47Z
title: "jx create cluster gke"
slug: jx_create_cluster_gke
url: /commands/jx_create_cluster_gke/
---
## jx create cluster gke

Create a new kubernetes cluster on GKE: Runs on Google Cloud

### Synopsis

This command creates a new kubernetes cluster on GKE, installing required local dependencies and provisions the Jenkins X platform 

You can see a demo of this command here: https://jenkins-x.io/demos/create_cluster_gke/

Google Kubernetes Engine is a managed environment for deploying containerized applications. It brings our latest innovations in developer productivity, resource efficiency, automated operations, and open source flexibility to accelerate your time to market. 

Google has been running production workloads in containers for over 15 years, and we build the best of what we learn into Kubernetes, the industry-leading open source container orchestrator which powers Kubernetes Engine.

```
jx create cluster gke [flags]
```

### Examples

```
  jx create cluster gke
```

### Options

```
  -b, --batch-mode                          In batch mode the command never prompts for user input
      --cleanup-temp-files                  Cleans up any temporary values.yaml used by helm install [default true] (default true)
      --cloud-environment-repo string       Cloud Environments git repo (default "https://github.com/jenkins-x/cloud-environments")
      --cluster-ipv4-cidr string            The IP address range for the pods in this cluster in CIDR notation (e.g. 10.0.0.0/14)
  -n, --cluster-name string                 The name of this cluster, default is a random generated name
      --default-admin-password string       the default admin password to access Jenkins, Kubernetes Dashboard, Chartmuseum and Nexus
      --default-environment-prefix string   Default environment repo prefix, your git repos will be of the form 'environment-$prefix-$envName'
  -d, --disk-size string                    Size in GB for node VM boot disks. Defaults to 100GB
      --docker-registry string              The Docker Registry host or host:port which is used when tagging and pushing images. If not specified it defaults to the internal registry unless there is a better provider default (e.g. ECR on AWS/EKS)
      --domain string                       Domain to expose ingress endpoints.  Example: jenkinsx.io
      --draft-client-only                   Only install draft client
      --enable-autoupgrade                  Sets autoupgrade feature for a cluster's default node-pool(s)
      --environment-git-owner string        The git provider organisation to create the environment git repositories in
      --exposecontroller-pathmode path      The ExposeController path mode for how services should be exposed as URLs. Defaults to using subnets. Use a value of path to use relative paths within the domain host such as when using AWS ELB host names
      --exposer string                      Used to describe which strategy exposecontroller should use to access applications (default "Ingress")
      --external-ip string                  The external IP used to access ingress endpoints from outside the kubernetes cluster. For bare metal on premise clusters this is often the IP of the kubernetes master. For cloud installations this is often the external IP of the ingress LoadBalancer.
      --git-api-token string                The git API token to use for creating new git repositories
      --git-private                         Create new git repositories as private
      --git-provider-url string             The git server URL to create new git repositories inside
      --git-username string                 The git username to use for creating new git repositories
      --global-tiller                       Whether or not to use a cluster global tiller (default true)
      --headless                            Enable headless operation if using browser automation
      --helm-client-only                    Only install helm client
      --helm-tls                            Whether to use TLS with helm
      --helm3                               Use helm3 to install Jenkins X which does not use Tiller
  -h, --help                                help for gke
      --http string                         Toggle creating http or https ingress rules (default "true")
      --ingress-cluster-role string         The cluster role for the Ingress controller (default "cluster-admin")
      --ingress-deployment string           The name of the Ingress controller Deployment (default "jxing-nginx-ingress-controller")
      --ingress-namespace string            The namespace for the Ingress controller (default "kube-system")
      --ingress-service string              The name of the Ingress controller Service (default "jxing-nginx-ingress-controller")
      --install-dependencies                Should any required dependencies be installed automatically
      --install-only                        Force the install command to fail if there is already an installation. Otherwise lets update the installation
      --keep-exposecontroller-job           Prevents Helm deleting the exposecontroller Job and Pod after running.  Useful for debugging exposecontroller logs but you will need to manually delete the job if you update an environment
  -v, --kubernetes-version string           The Kubernetes version to use for the master and nodes. Defaults to server-specified
      --labels string                       The labels to add to the cluster being created such as 'foo=bar,whatnot=123'. Label names must begin with a lowercase character ([a-z]), end with a lowercase alphanumeric ([a-z0-9]) with dashes (-), and lowercase alphanumeric ([a-z0-9]) between.
      --local-cloud-environment             Ignores default cloud-environment-repo and uses current directory 
      --local-helm-repo-name string         The name of the helm repository for the installed Chart Museum (default "releases")
  -m, --machine-type string                 The type of machine to use for nodes
      --max-num-nodes string                The maximum number of nodes to be created in each of the cluster's zones
      --min-num-nodes string                The minimum number of nodes to be created in each of the cluster's zones
      --namespace string                    The namespace the Jenkins X platform should be installed into (default "jx")
      --network string                      The Compute Engine Network that the cluster will connect to
      --no-brew                             Disables the use of brew on MacOS to install or upgrade command line dependencies
      --no-default-environments             Disables the creation of the default Staging and Production environments
      --on-premise                          If installing on an on premise cluster then lets default the 'external-ip' to be the kubernetes master IP address
  -p, --project-id string                   Google Project ID to create cluster in
      --prow                                Enable prow
      --recreate-existing-draft-repos       Delete existing helm repos used by Jenkins X under ~/draft/packs
      --register-local-helmrepo             Registers the Jenkins X chartmuseum registry with your helm client [default false]
      --skip-auth-secrets-merge             Skips merging a local git auth yaml file with any pipeline secrets that are found
      --skip-ingress                        Dont install an ingress controller
      --skip-installation                   Provision cluster only, don't install Jenkins X into it
      --skip-login                          Skip Google auth if already logged in via gloud auth
      --skip-tiller                         Don't install a Helms Tiller service
      --subnetwork string                   The Google Compute Engine subnetwork to which the cluster is connected
      --tiller                              Whether or not to use tiller at all. If no tiller is enabled then its ran as a local process instead (default true)
      --tiller-cluster-role string          The cluster role for Helm's tiller (default "cluster-admin")
      --tiller-namespace string             The namespace for the Tiller when using a gloabl tiller (default "kube-system")
      --timeout string                      The number of seconds to wait for the helm install to complete (default "6000")
      --tls-acme string                     Used to enable automatic TLS for ingress (default "false")
      --user-cluster-role string            The cluster role for the current user to be able to administer helm (default "cluster-admin")
      --username string                     The kubernetes username used to initialise helm. Usually your email address for your kubernetes account
      --verbose                             Enable verbose logging
      --version string                      The specific platform version to install
  -z, --zone string                         The compute zone (e.g. us-central1-a) for the cluster
```

### SEE ALSO

* [jx create cluster](/commands/jx_create_cluster/)	 - Create a new kubernetes cluster
* [jx create cluster gke terraform](/commands/jx_create_cluster_gke_terraform/)	 - Create a new kubernetes cluster on GKE using Terraform: Runs on Google Cloud

###### Auto generated by spf13/cobra on 17-Sep-2018
