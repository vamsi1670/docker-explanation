# docker-explanation
DOCKER 
what is DOCKER:
-> docker is software container platform and container management service.
->It is the 	environment where things run.
->The whole idea of Docker is for developers to easily develop applications, ship them into containers which can then be deployed anywhere.
->The initial release of Docker was in March 2013.
->applications runs or behaves faster than in docker containers compare to virtual machines. 
HUB:
->Docker Hub is a registry service on the cloud that allows you to download Docker images that are built by other communities. You can also upload your own Docker built images to Docker hub.
IMAGES:
->In Docker, everything is based on Images. An image is a combination of a file system and parameters.
->To see the list of Docker images on the system, you can issue the following command.
    syntax---> docker images
->Each image has the following attributes -

TAG - This is used to logically tag images.

Image ID - This is used to uniquely identify the image.

Created - The number of days since the image was created.

Virtual Size - The size of the image.
->Images can be downloaded from Docker Hub using the Docker pull command. 
example:docker pull imagename->this command pulls the image from remote pull to local repo.
                  docker run imagename -> this command pulls the image from remote repo to local repo and creates a container for the image.  
->Image - This is the name of the image which is used to run the container.
                  --- every  image has its own image name and image id.
                  --- by using image id or name we can remove the image from local repo                     
                   ---> example:docker rmi ImageID
                   ---> docker images -q
                   ---> q - It tells the Docker command to return the Image ID’s only.
----> DOCKER INSPECT:
->This command is used see the details of an image or container.
Syntax
docker inspect image name/container name
CONTAINERS:
Containers are instances of Docker images that can be run using the Docker run command. The basic purpose of Docker is to run containers.
->by using image we can create container.
example:docker run imagename/id
->we can create multiple containers with the same image.
->while we launching container its creates an userspace or isolated space.
->isloated space is nothing but the space  which is not  sharing with anyone.
->containers can be stop/start by using its id or name.
->to remove the container we use "rm" command
->to remove forcefully we use  docker rm containerid --force. it means it removes the containers which are running.
->docker ps to see  containers which are running
->docker ps -a to see all the containers and can check the status 
->some containers expects dependencies.
->in containers we use to deploy applications. the best practise is every conatiner should have only one application.we can also have one or more apps but it effects on the performance on the container.
-> to associate two or more containers by using link 
->the containers would communicates with tcp or http protocols.
->applications considers that container as a O.S,whereas our hostos considers container as a process.
->within every container it has its own virtual file system.where it starts from root.
->this file system seems like a full blown O.S for application.
->docker LOGS: it gives the commands which are we executed in the container. 
->container starts with two modes detached mode and interactive mode
->detached mode (-d):it runs in background and it simply gives id the container.
->interactive mode(-i):it is the default mode of the container.it runs in foreground.the use of this mode is we can quit the container while  it is running by using control+c.
                                           :we can see clearly what is happening when container is creating  i.e while docker running.
->interactive mode(-it):this means that you are saying to container what to b done.
                                             :it is not possible in -i mode.this process generally we do in devlopment process.
->port mapping cannot be possible for the running containers.
->increasing memory size can be possible for running containers.
 TAG:
It is nothing but a version of the image
ex:docker pull jenkins:3.1->tag
->Tags are useful to run or pull a particular image 
KERNEL NAMESPACE:
->isolated environments are created by KERNEL NAMESPACE.
->docker completely relies on kernel namespace.
->namespaces makes  docker to work.
->namespaces are used by your host O.S to create a container.
CONTROLGROUP:
->c-group are used to control anything in containers.
->which allocates memory to our containers.
CAPABILITIES:
->capabilities are from user namespace.which gives permissions or privilages. 
