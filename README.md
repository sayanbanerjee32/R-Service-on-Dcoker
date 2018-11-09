
This is part 1 and this describes how to deploy single instance of a R service on docer

## Example R service code:
 
 
 <img src="screenshots/R_service.png" alt="hi" class="inline"/>

## Folder structure:   
No need to have the start service file. Only following required:
1.	prediction code with plumber
2.	Model rda files and any other reference files
3.	Dockerfile
 
<img src="screenshots/folder_structure.png" alt="hi" class="inline"/>

 
## Dockerfile: 
In our case we'll need to have additional copy statements for rda files and all other reference files.
Note the command to install required R packages. All required R packages are need to be installed explicitly (not plumber)
 
<img src="screenshots/docker_file.png" alt="hi" class="inline"/>
 
 
## Build docker image:
Note how folder structure is provided in the build command (here Dockerfile should reside)
This will also install all the required R packages (as per Dockerfile) at the end (may take some time)

<img src="screenshots/build.png" alt="hi" class="inline"/>
 
## Docker image repository: 
See plumber image is now downloaded as well
 
<img src="screenshots/repository.png" alt="hi" class="inline"/>
 
## Run new docker image and see it is running
 
<img src="screenshots/run.png" alt="hi" class="inline"/>
 
## To know docker machine IP:

<img src="screenshots/ip.png" alt="hi" class="inline"/>

 
## Invoke the Service: 
Use Ip address from above and port form docker run command

<img src="screenshots/response.png" alt="hi" class="inline"/>

