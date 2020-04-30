Hi, I am Abhilash from PRSCET , Trivandrum.

This is my first project on Docker, based on the concepts learnt from the online sessions of Mr. Vimal Daga.

The project is done inside Docker in Red Hat Enterprise Linux 8 (RHEL V-8). 
Dockeris  a  system that  provides pre-configured, self-contained applications, frameworks, and software stacks, 
such as WordPress, Golang, or LAMP. Even entire Linux  distributions can  be run in  Docker. When deployed, 
these software packages are referred to as containers.  Docker also allows you to create your own containers that 
include any custom software.

Docker Compose is a complementary system which helps you link together individual Docker containers so they can 
work together. 

This guide walks through the deployment of a Joomla container and another MySQL container that Joomla will use 
to store its data. Docker Compose will facilitate the networking between them.

Containers for Joomla and MySQL are available from Docker Hub in the form of images. 
A Docker image is a static snapshot of a container which is used to create new container instances.


PROJECT OBJECTIVE
------------------
Confiruration of Joomla server and mySQL server on Docker containers and connecting between them.

PREREQUISITES:
-----------------

In order to complete the steps in this guide, you will need the following:

1. Root access to the OS.
2. YUM properly configured
3. Docker installed
4. MySQL image installed
5. PhpMyAdmin and Joomla images installed


STEP 1: Prior to running the docker services, you are required to disable the firewall
and SELinux using the following command:
      systemctl stop firewalld

STEP 2: Disabling the SELinux:
       setenforce 0

STEP 3: Start docker services:
systemctl start docker

STEP 4: Pull the latest version of Joomla and phpmyadmin docker images from hub.docker.com
docker pull joomla:latest
docker pull phpmyadmin/phpmyadmin

STEP 5 Pull the latest version 5.6 of MySQL docker image from hub.docker.com
docker pull mysql:5.6

STEP 6: To see all docker images:
docker images

STEP 7: Create a directory named “joomla” in the root folder:
mkdir joomla

STEP 8: Create a file named “docker-compose.yml” inside the “joomla” directory.
cd joomla
vim docker-compose.yml

STEP 9: Enter the source code

STEP 10: Run the docker-compose file: docker-compose up

STEP 11: Inpect the Joomla container using its container ID:
docker inspect [CONTAINER ID]

STEP 12: Get the IP address of Joomla container.

STEP 13: Open the browser and browse with URL:
        10.10.100.20:8092

STEP 14: Proceed with the Joomla installation steps and finish configuring the website.







