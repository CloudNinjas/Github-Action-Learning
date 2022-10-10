# Chapter 5: Infrastructure deployments

Here we will summarize some use cases for GitHub Actions and deploying, updating, or deleting infrastructure components and its benefits.

## Why

For deploying infrastructure in my opinion the key is consistency.
If you work with the common cloud providers and their services you notice really fast how hard it is to keep up with the changes. Being able to know every single service of just one cloud provider becomes in this day and age a huge difficulty. If you work with so many services you somehow need to relay on a team consisting of various people with different sills. But at the end every single of them need to be able to be able to deploy your services and be able to recover failed deployments or be able to understand why something is breaking. To do so having an consistent base how to deploy services is important.

## How to achieve the key consistency

The first step towards the goal is to use tools like [terraform](https://www.terraform.io/), [packer](https://www.packer.io/), [ansible](https://docs.ansible.com/), [crossplane](https://crossplane.io/), [AWS Cloud Formation](https://aws.amazon.com/cloudformation/), [Azure Resource Manage](https://learn.microsoft.com/en-us/azure/azure-resource-manager/management/overview), or [Google Cloud Deployment Manager](https://cloud.google.com/deployment-manager/docs) to just name a few. This tools are grouped under the term of Infrastructure as Code.

The second step is to create, in the case of terraform, modules to have your configuration, that is necessary for your service to work, defined in your modules.

The third step is to recreate the calls to your modules in such a way that you deploy every service in the same way.

All of the steps above are helping to build consistent infrastructure deployments and to avoid facing simple issues over and over again.

## Recreating the calls to your modules

With "recreating" we mean to be able to create default deployments easy as possible and without having to setup every component individually.
To achieve this we combine predefined templates, versioned modules, and GitHub Actions.

+ **Predefined templates:** This are tested module calls to create the service.
+ **Versioned modules:** This are versions for your modules to be able to refer why deployments might break and to be able to support older versions of your modules.
+ **GitHub Actions:** Pipeline solution we prefer at the moment.