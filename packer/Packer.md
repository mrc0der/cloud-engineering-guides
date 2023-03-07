# Introduction to Immutable Architectures and Packer

Immutable architectures are becoming increasingly popular as a way to deploy applications and services in the cloud. By using immutable architectures, you can ensure that your applications and services are always running the same version of code, with no manual intervention required. This makes it easier to manage deployments, as well as making them more secure. In this lab, we will explore the benefits of immutable architectures, and how to use Packer to build Amazon Machine Images (AMIs).

## What is an Immutable Architecture?

An immutable architecture is a type of software architecture where components are not modified after they have been deployed. This means that once an application or service has been deployed, it cannot be changed or updated in any way. Instead, any changes must be made by deploying a new version of the application or service. This ensures that all components are always running the same version of code, which makes it easier to manage deployments and keep them secure.

## What is Packer?

Packer is an open source tool for creating machine images for multiple platforms from a single source configuration. It automates the process of creating machine images for different cloud providers such as Amazon Web Services (AWS), Microsoft Azure, Google Cloud Platform (GCP), DigitalOcean and more. Packer can be used to build AMIs for AWS EC2 instances, which can then be used to create new instances with pre-configured settings and software packages installed.

## Lab Exercise: Building an AMI with Packer

In this lab exercise we will use Packer to build an AMI for an AWS EC2 instance. We will use a simple configuration file written in JSON format to define our image settings and software packages that need to be installed on the instance.

### Step 1: Install Packer

The first step is to install Packer on your local machine. You can download the latest version from [here](https://www.packer.io/downloads/). Once you have downloaded the package, follow the instructions provided by Packer's documentation to install it on your system.

### Step 2: Create Configuration File

Once you have installed Packer on your system, create a configuration file in JSON format that defines all of the settings for your image and any software packages that need to be installed on it. Here is an example configuration file:

    {   "builders": [{   "type": "amazon-ebs",   "region": "us-east-1",   "source_ami_filter": {     "filters": {       "virtualization-type": "hvm",       "name": "amzn2-ami-hvm*",       "root-device-type": "ebs"     },     "owners": ["amazon"],     "most_recent": true   },   }],   "provisioners":[{     "type":"shell",     "inline":[       “sudo apt update”,       “sudo apt install -y nginx”    ] }] }

This configuration file tells Packer that we want it to create an Amazon EBS image in us-east-1 region using the most recent HVM AMI available from Amazon (specified by `source_ami_filter`). It also tells Packer that we want it to install Nginx web server on our image (specified by `provisioners`).

Once you have created your configuration file save it as `packer_configuration.json`.

### Step 3: Build Image with Packer

Now that you have created your configuration file you can use Packer's command line interface (CLI) tool `packer`to build your image from it:

    packer build packer_configuration.json

This command will tell packer to read our configuration file `packer_configuration`and create our image according to its settings specified in the file . Once packers finishes building our image ,it will output its ID which we can use later when creating EC2 instances from our newly created AMI .
