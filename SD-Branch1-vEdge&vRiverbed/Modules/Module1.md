## NFV-Automation

### Environment Variables and Collection

The files inside the code folder contain an environment file, a collection file,
an input data file, and a vEdge-Cloud configuration file.  

The environment file and collection file can be imported into your local Postman
application.  These setup the various APIs that will be used as part of the testing.

After importing the Collection, note it is comprised of two folders and a couple
of extra API commands.  The first folder contains a series of API calls used to instantiate a VNF on
NFVIS.  The second folder is used for cleanup.  

![alt text](../images/Postman-Collection_Import.png)

Opening the folder "Instantiate vEdge on CSP" shows a list of API calls that would be used serially in order to build up the components inside NFVIS such as downloading the image, creating the virtual bridges and networks, and mapping those virtual networks to the correct physical interface on the CSP.  Once those components are enabled, the final API call spins up the vEdge.

With all of these API calls, there are several variables used.  For variables that would be the same throughout the entire environment, Environent Variables are used.  For those that might change for each device, a list of data is provided in a JSON fomatted structure.  

We will explore some of these individual APIs in the next step.

Near the top right of Postman, you set your Environment.  Since you just imported an Environment file, let's select that one to use for our testing.  It is called **NFV-Environment**

![alt text](../images/Postman-Changing_Environment.png)

Once you have selected the environment, click on the eye icon to the right to examine the variables.  There are four variables that are part of the Environment settings:  

* NFVIS IP Address
* Content-Type (What format in which we'll send data to NFVIS)
* Accept (What foramt in which we want to receive data from NFVIS)
* FTP Server Path

Leave the *Content-Type* and *Accept* variables alone.  Modify the IP address and FTP path for your system.

![alt text](../images/Postman-Modifying_Environment_Variables.png)


### [Next Step - Exploring The First API Call](Module2.md)
