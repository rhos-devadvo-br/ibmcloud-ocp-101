# Red Hat OpenShift Kubernetes Service at IBM Cloud 101

<br>
<br>
<div align="center">
    <img width="50%" src="./docs/imgs/rhos-logo.png" alt='video'>
</div>
<br>
<br>

## The leading multicloud container development platform

Red Hat OpenShift is named a leader across 29 criteria and 8 major vendors by the [Q3 2020 Forrester Wave report](https://www.openshift.com/2020-forrester-wave?hsLang=en-us).

## What's the difference from Kubernetes?

The main difference from Kubernetes is that OpenShift is a **product** with enterprise support that requires a paid subscription, while Kubernetes is a "project". OpenShift is built on top of the [OKD](https://www.okd.io/) project, a Kubernetes distribution optimized for continuous application development and multi-tenant deployment. OKD adds developer and operations-centric tools on top of Kubernetes to enable rapid application development, easy deployment and scaling, and long-term lifecycle maintenance for small and large teams. OKD is free to use and has the core features of OpenShift, but without the enterprise support that comes with the paid Red Hat OpenShift subscription. OpenShift, like OKD and Kubernetes, is also completely open-source. You can see the code for yourself at [GitHub](https://github.com/openshift/).

## Red Hat OpenShift offerings and costs

Red Hat OpenShift clusters can be "managed" or "self-managed". Managed cluster's compute and network infrastructures are hosted and managed by cloud providers while self-managed clusters need to be installed from scratch - they can be installed on traditional cloud infrastructure nevertheless. A full list of supported cloud providers which have managed OpenShift offerings can be viewed [at the official OpenShift homepage](https://www.openshift.com/products/pricing/).

OpenShift clusters have a Red Hat monthly license cost attached, while the compute and network infrastructure costs are paid to a specific cloud provider and vary depending on the allocated resources and specific provider's price plans.

## Creating a managed OpenShift cluster at IBM Cloud

There are two types of managed OpenShift clusters "as a Service" at IBM Cloud: a cluster created with classic infrastructure, or one created with a Virtual Private Cloud (VPC) infrastructure. VPC clusters have a virtual network layer built on top of the Virtual Servers Instances (VSI's). This network layer provides isolation and improved personalization capabilities such as custom network security policies for the subjacent compute infrastructure. VPC infrastructure is not yet available at South America.

- [Provison a Virtual Private Cloud](https://cloud.ibm.com/vpc/provision/vpc) (Optional)
- [Provison a managed OpenShift cluster](https://cloud.ibm.com/kubernetes/catalog/create?platformType=openshift)

When provisoning the OpenShift cluster at IBM Cloud, you'll setup the following:

- OpenShift version (3.11, 4.4, or 4.5)
- Purchase of additional OCP licenses or application of an existing Cloud Pak OCP entitlement license
- Infrastructure type: Classic, VPC, or Satellite (new)
- Location (AZs and subnets)
- Worker Pool (vCPUs, Memory, nº of worker nodes)

### Details for VPC clusters

1. If you choose to create a VPC cluster you need to have at least three subnets (one in each AZ).
2. Each subnet must have a Public Gateway attached, otherwise you won't be able to access your cluster through the Internet.
3. If you check your Load Balancers at the [IBM Cloud VPC panel](https://cloud.ibm.com/vpc-ext/network/loadBalancers) you will see that OpenShift creates one automatically for you.

## Accessing your cluster

Access the [IBM Cloud Resources List](https://cloud.ibm.com/resources) and click on the previously created cluster. You'll be redirected to the managed cluster administration page at IBM Cloud, where you can check access, overview worker node's status, create new worker pools, install add-ons and attach IBM DevOps solutions to your cluster.

### Using the Web Console

To access the OpenShift Web Console you can simply click on the blue button, as indicated on the image below.

<br>
<div align="center">
    <img width="80%" src="./docs/imgs/accessing-web-console.png" alt='video'>
</div>
<br>

### Using the OpenShift CLI (oc)

[Download the OpenShift CLI (oc)](https://mirror.openshift.com/pub/openshift-v4/clients/oc/) that matches your local operating system and cluster version. For information about how to install the CLI, [see the docs](https://cloud.ibm.com/docs/openshift?topic=openshift-openshift-cli#cli_oc). For OpenShift 4.5 check [this link](https://mirror.openshift.com/pub/openshift-v4/clients/oc/4.5/).


