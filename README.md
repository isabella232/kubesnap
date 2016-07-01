# kubesnap

## How to run
1. [Prerequisites](#1-prerequisites)  
2. [Start work with Google Cloud Platform](#2-start-work-with-google-cloud-platform)  
3. [Install kubesnap](#3-install-kubesnap)
4. [Contributing](#4-contributing)  
5. [License](#5-license)  
6. [Acknowledgements](#6-acknowledgements)  

### 1. Prerequisites

- **Kubernetes** cluster - tested with Kubernetes on Google Cloud Environment (GCE)

### 2. Start work with Google Cloud Platform

#### a) Open Google Cloud Platform Console
 - go to https://console.cloud.google.com/  
 - log in using your e-mail address
 - follow the instruction [how to create a Cloud Platform Console project](https://cloud.google.com/storage/docs/quickstart-console)


#### b) Select your project  
- select your project from the drop-down menu in the top right corner
  ![Alt text](docs/images/image_01.png "Selecting a project in Cloud Platform Console")  

#### c) Switch to _**Compute Engine**_ screen

- select _Products & Services_ from GC Menu in the top left corner  

  ![Alt text](docs/images/image_02.png "Google Cloud Console Menu") 

- and then select _Compute Engine_ from the drop-down list

  ![Alt text](docs/images/image_03.png "Selecting Compute Engine in Google Cloud Console Menu")

#### d) Create an VM instance  
- create a new VM instance
  ![Alt text](docs/images/image_04.png "Creating an VM instance")  

- set an unique name of a new instance
- choose a machine with 4 vCPUs (or more) and at least 15GB RAM
- select Ubuntu 16.04 with standard persistent disk with at least 100GB

  ![Alt text](docs/images/image_05.png "Setting up a new VM")  

#### e) Start GCE Virtual Machine  
- select your VM and choose _START_ option which is available on the top of screen

  ![Alt text](docs/images/image_06.png "Staring an VM instance")  

#### f) Open the VM terminal by click on SSH  
 -  click on SSH to open the VM terminal (it will open as a new window)

  ![Alt text](docs/images/image_07.png "Opening the terminal of Virtual Machine") 

#### g) Authorize access to Google Cloud Platform  
- manage credentials for the Google Cloud SD. To do that, run the following command:
  ```
  gcloud auth login
  ```
  Answer `Y` to the question (see below) and follow the instructions:
  -	copy the link in your browser and 
  -	authenticate with a service account which you use in Google Cloud Environment,
  - copy the verification code from browser window and enter it

  ![Alt text](docs/images/image_08.png "Access authorization to Google Cloud Platform")

- check if you are on credentialed accounts:  
 ```
 gcloud auth list
 ```


### 3. Install kubesnap  
Clone kubesnap into your home directory:
```
git clone https://github.com/intelsdi-x/kubesnap
```
kubesnap supports automatic installation via script [provision-kubesnap.sh](https://github.com/intelsdi-x/kubesnap/blob/master/tools/provision-kubesnap.sh)

Go to kubesnap/tools:
```
cd kubesnap/tools
```

##### Building

- Build kubesnap:
```
./provision-kubesnap.sh
```

- Build Kubernetes:
```
./provision-kubesnap.sh --kubernetes build
```
##### Starting
- Start Kubernetes cluster:
```
./provision-kubesnap.sh --kubernetes start
```  

### 4. Contributing
We love contributions!

There's more than one way to give back, from examples to blogs to code updates. See our recommended process in [CONTRIBUTING.md](CONTRIBUTING.md).

And **thank you!** Your contribution, through code and participation, is incredibly important to us.

### 5. License
[snap](http://github.com:intelsdi-x/snap), along with this kubesnap, is an Open Source software released under the Apache 2.0 [License](LICENSE).

### 6. Acknowledgements
* Author: [Andrzej Kuriata](https://github.com/andrzej-k/)
