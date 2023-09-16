# Camunda Platform 8 Self Managed - One Click Installation

![Compatible with: Camunda Platform 8](https://img.shields.io/badge/Compatible%20with-Camunda%20Platform%208-0072Ce)

[![](https://img.shields.io/badge/Community%20Extension-An%20open%20source%20community%20maintained%20project-FF4700)](https://github.com/camunda-community-hub/community)

[![](https://img.shields.io/badge/Lifecycle-Proof%20of%20Concept-blueviolet)](https://github.com/Camunda-Community-Hub/community/blob/main/extension-lifecycle.md#proof-of-concept-)

Camunda 8 Platform Self Managed can be installed using officially supported [Camunda 8 Helm Charts](https://github.com/camunda/camunda-platform-helm)

However, before installing Camunda, you'll need a kubernetes cluster, and will also most likely want to provision a domain name, tls certificates, and install an ingress controller.

The [Camunda 8 Helm Profiles]() community project can assit you to setup all this infrastructure, but it can be tedious to set up all the tools needed such as `make`, `kubectl`, and `helm`, not to mention the cloud provider tools such as `aws cli`, `eksctl`, `gcp cli`, `azure cli`, etc. 

So, this project, the `C8SM-One-Click-Install` takes an interesting approach. What if we use Camunda 8 to install Camunda 8?! It turns out that this works really well! This project describes how to use Camunda 8 to easily provision additional Camunda 8 SM environments with a single click. 
## Getting Started

### Step 0 - Chicken vs the Egg

So, there's only one *small* problem. We need a C8 SM environment to install a C8 SM environment :flushed:

As of September 2023, you'll need to sign up for a Camunda 8 SaaS trial account. 30 day trial accounts are available for free at [https://signup.camunda.com](https://signup.camunda.com)

> [!NOTE]  
> This project uses start forms. Therefore, you'll need to use an 8.3.x version. As of September 2023, be sure to choose to create a `8.3.0-alphaX` cluster.

> [!NOTE]
> It will also be possible to use [Docker Compose](https://github.com/camunda/camunda-platform) to perform a local install of Camunda 8 SM once version `8.3` is officially released.

### Step 1 - Deploy the BPMN Files

Open your Camunda SaaS Modeler, upload the files found in the [bpm](bpmn) directory, and deploy each bpmn diagram to a `8.3.x` cluster. 

> [!NOTE]  
> It will also be possible to use Docker compose after 8.3 is officially released.  

