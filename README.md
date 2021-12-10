<div style="margin-bottom: 1%; padding-bottom: 2%;">
	<img align="right" width="100px" src="https://dx29.ai/assets/img/logo-Dx29.png">
</div>

Dx29 Pipelines All
==============================================================================================================================================
### **Overview**

In this project the YAML of a environment pipeline and the manifest files needed to deploy the environment will be located.

There will be a single YAML that has access to the different repositories or projects (microservices) and uses templates to build the images of each of them and deploy them in the environment. In this way, there will be a main pipeline that will use as templates those of the different components.

>- Azure-pipelines.yaml is the main file.
>- Folder templates contains the YAML files for each component.
>- Folder manifests contains the manifests for each component (deployment and service)

For each component, the repository where the source code is located will be accessed. Each of the files that appear in Templates and manifest are copies of the manifests and pipeline project files for each component.


The main pipeline:

>- It will configure the access to the different code repositories.
>- It will define the variables to work with.
>- And it will include as a stage each of the templates implemented for each component of the application, passing the values of the previous variables as parameters.

Finally, this pipeline will also have an input parameter that can be used for version control. When this pipeline is launched, a Tag or version will be indicated so that:
>1. All images of the application components with that tag will be compiled and uploaded to the container registry.
>2. Deploy the images with the tag indicated in the cluster (AKS).

Therefore, the execution of this pipeline is manual.

It is used in the [Dx29 application](https://dx29.ai/) and therefore how to use and integrate it is described in the [Dx29 architecture guide](https://dx29-v2.readthedocs.io/en/latest/index.html).

<p>&nbsp;</p>

### **Getting Started**

####  1. Configuration: Pre-requisites

This project doesn’t need any dependency or secret.

You need an [Azure Pipelines](https://azure.microsoft.com/en-gb/services/devops/pipelines/) environment to run it. 

<p>&nbsp;</p>

####  2. Download and installation

Download the repository code with `git clone` or use download button.
You can use any text editor with this project.

You must work on a repository on Github and have it associated with this project and Azure Pipelines to run it.

<p>&nbsp;</p>

### **Contribute**

Please refer to each project's style and contribution guidelines for submitting patches and additions. 

In general, we follow the "fork-and-pull" Git workflow.

>1. Fork the repo on GitHub
>2. Clone the project to your own machine
>3. Commit changes to your own branch
>4. Push your work back up to your fork
>5. Submit a Pull request so that we can review your changes

The project is licenced under the **(TODO: LICENCE & LINK & Brief explanation)**

<p>&nbsp;</p>
<p>&nbsp;</p>

<div style="border-top: 1px solid !important;
	padding-top: 1% !important;
    padding-right: 1% !important;
    padding-bottom: 0.1% !important;">
	<div align="right">
		<img width="150px" src="https://dx29.ai/assets/img/logo-foundation-twentynine-footer.png">
	</div>
	<div align="right" style="padding-top: 0.5% !important">
		<p align="right">	
			Copyright © 2020
			<a style="color:#009DA0" href="https://www.foundation29.org/" target="_blank"> Foundation29</a>
		</p>
	</div>
<div>