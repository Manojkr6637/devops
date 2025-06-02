Day-1====
devops
 -CI/CD
 -Improving delievery
 -Automation
 -Quality
 -Monitoring
 -Testing
 Devops is a process of improving the application delievery
    -Automation
	-Quality
	-Continues & Monitoring
	-Continues Testing
System Admin:-Server(VMware, Openstack,xen)
BRE-Build, Release Engineer->Deploy
Server Admin->
Automation Engineer
============Day-2======
Software Development Life Cycle(SDLC)
Design
Develop   High Quality
Test


Eg.   E-commerce
  
    Planing->Defining->Designing(HLD,LLD)->Building->Testing->Deploy
	
	Devops->(Building, Testing, Deploy) phase->Automation
	
	
	Building:
	    -Developing->common Location->Git(Source Code Repository)
	Testing:
	    -Testing, Quality Engineer
	Deployment: Prod
===============Day-3=================
Virtual Machine(VM) part-1

-What is a server?
-Physical(VS) Virtual
-Hypervisor
-How to create VM
-Real World Example

   Efficiency->Hypervisor->(VMware,xen)
   Logical Isolation
   ->Memory, CPU, Hardware->logical isolation
   
=============Day-4============
Virtual Machine part-2


Aws  Azure

VM->EC2

API
   -AWS EC2
   -Request
   -EC2 instatie
   
      valid
	  authenticate
	  Authorized
	  
Script
 AWS CLI
 AWS API(Python-Boto3)
 AWS CFT(Cloud Format Template)
 Terraform(Advance)(AWS, Azure, Google Cloud)
 AWS CDK->new Advance
 
 --
   What is Virtual Machine->Infrastructure->EC2 is infrastructure
   
   Hybrid cloud platform->best teraform
   Kubertnetes
   
 



Connect to windows EC2 ->MobaXterm, nomachine


==================Day-23===




Model-2           Model 1
c1, c2            c1, c2     
Docker            Docker  
vm/EC2            OS 
                 IBM/HP
				 
Docker container->Light width->package->(Applicatios+Libraries+System Dependencies)		
Container has base image(minimul os)		 


============Day-5================Z
item

Mac laptop
52.66.29.163 public IP
user: ubuntu

--------Connect to terminal===
ssh ubuntu@52.66.29.163
ssh -i(identity) /manoj/user.pem ubuntu@52.66.29.163
or ssh -i user.pem ubuntu@52.66.66.29.193


aws cli interface download
https://aws.amazon.com/cli/
for windows
cmd>aws --version
-users->security->access key
aws configure
enter access key
enter access password
default region:ap-south-1
default file format:json
#create new s3 bucket;
aws s3 mb s3://mybucket-test-aws-cli
aws s3 ls->list s3 bucket
#Another way to aws api

AWS cloudFormation sample templates
iaas


boto3-aws configuration
===============Day-6======================
#linux Operatin System and Basics of Shell scripting
  -Free
  -Open Source
  -Secure
  -Distribution
  -Fast
  -
    CPU, Memory, IO
    OS
	Kernel
	System Libraries(libc)
	System Software
	User process
	compilers
	Kernel: Heart of Linux OS which establish connections between HW and Software
	  -Device Mgt
	  -Memory Mgt
	  -Procss mgt
	  -Handing System call
#Shell Scripting
   >bash
   >psd(present working directory)
   >cd(change directory)
   >cd ../..(two directory)
   ls -ltr(whole detail)
    touch test.txt
	vi test.txt(create and edit)
	:wq!(save the file
	cata text.txt
	mkdir(create dir)
	rm -r testDir
	free -g(memory of laptop or server)
	nproc(no of processor)
	df -h(memory users)
	top(all details)
========= Day-7=============
EC2
S3
Lambda
IAM

 ======
  
 
>bash 
ubuntu
sudo yum remove awscli
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
which aws
ls -l /usr/local/bin/aws
=============Q. How to track resources user in aws writh shell scripting========
vim aws_resource_tracker.hs
escape->insert
#!/bin/bash

#########################################
#Author Manoj
#Date: 11th-Jn
#Version:v1
#This script will report the aws resource usage
###############

# AWS S3
# AWS EC2
# AWS Lamda
# AWS IAM Users

set -x
#list S3 buckets
echo "Print list s3 buckets"
aws s3 ls>resoruceTracker(redirect file)

#List EC2 instances
echo"Print list ec2 instaces"
#aws ec2 describe-instances
aws ec2 describe-instances  | jq '.Reservations[].Instances[].InstanceId'>resourceTracker:q!

#list lambda
 echo "Print list lamda"

aws lambda list-functions

#list IAM Users
 "Print list of users"

aws iam list-users

=============
ctrl+c
:qa->exit
:wq!->save and exit
>chmod 777 aws_resource_tracker.sh
./aws_resource_tracker.sh->execute
./aws_resource_tracker.sh->execute | more->get more details
 
 ======================day-8============== 
 Shell script
   github integration
   kubernetes
   kubectl
 API or CLI
 ubuntu:shell-scripting-example:13.232.91.205
 git token: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
 ./list-users.sh Manojkr6637 netflix-gpt->execute
=====================Day-9===============
git and github
 CSV->Centralized
 SVN->Centralized
 Git->Distributed
 
 git 
   fork->copy of whole project(interview)
 SVN/CVN(Linux)
   ->Down
   Not communcate each other
git & gibhub
  -open source
  -EC2
  -Donwload
  
github(gitlab/bitbucket)
  -usuability
  -commenting
  -reviewing
  -project mgt
  
  
>ls -la(hidden files)
git diff
git reset --hard hashcode
cat caluclator.sh
==============Day-10===========
git branch
  main/master
     feature
	 
	 ->Release branch
	   hot fix branch(Production)
===============Day-11=====
git command for devops
How to create or initialize a git repository
git init
ls -a
ls -ltra
git add & git commit
git add && git commit -m "" && git push
git remot add ""
ssh-key -t rsa
vim /home/ubuntu/.ssh/id_rsa
cd .ssh
ls
#Clone vs fork->interview

fork:create copy of repository
clone:download of repository

rm -rf argo-cd
git branch -b  division
git log
git checkout main
#git merge, git rebase, git cherry-pick
git log division or git cherry-pick
git checkout division && git log

=============================Shell scripting====================

Manual ->automated
Reduce manuanl work

day to day activies task->automated
examples:
#!/bin/bash->linking
#!->called shebang


somebody using    #!/bin/bash or dash or sh or ksh or more 

#!/bin/bash->inform linux or unix kerne
       bash or dash or sh or ksh or more most widely use and almost sytax is common
	   
	   Very widely is bash
	   
	   
Differ: #!/bin/sh                          #!/bin/bash
	   linked or redicting
	   to #!/bin/bash
	   
	   
	   ubuntun use widely->#!/bin/dash
	   
	   always use default->#!/bin/bash
	   
	   
	   Some operating system decided #!/bin/dash by default
	   
	   Always careful
	   
	   
	   Interview Questions->  #!/bin/sh or #!/bin/bash or #!/bin/dash
	   
	   
	   
	   
	   
	   

test.txt
vi test.txt

chmod 777 test.txt
exectue files
  sh test.txt
  or
  ./test.txt
default vi file editor avaiable


any executeable file(sh,or python or other) in linux->  ./test.sh

sh first.txt ->file for executable

Linux ->security-

in Linux who exectuable the file



ls->list file and folder
ls -ltr ->list file and folders
touch-> create file and folder 
man(manual) find info
history

touch cmd for automation

Chmod xxx a.txt grand perission

chmod ->    root user
            group user
			all your user
			
pattern: v(root) v(group) v(user)	->all user


7(myself)7(my group)7(everyone)

In linux:
4->read
2->write
1->Execute

444->read, read, read


       		

 Root user->admin
 Group user->group
 Everyone->Whole user

  4->read
  2->write
  1->Execute
    chmod 444 a.txt->read root user, read group euser
	       
 cat cmd 
ls
chmod
history


vi test.txt  ->esc-I->insert
                 :wq!->save file
                  :qa for quite or :q
				  escp->colon->exit
				  :q for quite file
PWd->present working direcor
mkdir
cd change directory


1. sample-shell-scipt.sh
 #!/bin/bash
 
 # create a folder
  mkdir manoj
  
  cd manoj
  touch t1.txt t2.txt
  
  
  ===execute file===
  
  sh sample-shell-script.sh
  or 
  chmod 777 ./sample-shell-script.sh
  ./sample-shell-script.sh
  
  
 rm -rf manoj->delete folder and files 
 
 ====Why shell scripting for devops====
 
 infra maintaince     code repository(linux)           configuration managaement
 
 
 
 John->devops->10000 vms->linux->node health
 
 
    cpu 
	memory
	linux
	write shell scripting and execute on the local machine get all reports
	
	
	Scripting
	
	  login in 10000 machines ->send email  for 10000 machine reports
	  
	  10 machine supecions
	  3 memory
	  3 cpu
	  
	  
	  
	  Monitoring cpu and RAM
	  
	  cpu     RAM
	  
	   |        |  
	  nproc     Free
	  
	  
	  use top for all detail
	  
	  
	  df command for file system
============================Video2====

custom node
1. exaple:
# This script outputs the node healht

# Version: v1

##########


df -h->file system

free -g->memoeyr

nproc->process
===========
2. Example:

echo "Printing-----"

df -h->file system

echo "Memory-----"

free -g->memoeyr

echo "Process-----"

nproc->process

example: 3

set -x # debug mode for beginning of the script


ps -ef(entire process full details)

every virtual machine by python running
| pipe command pass first parameter to second command
ps -ef | grep "amazon"


interview Questions:

date| echo "date is..."

date is default command and pass to stdin channel,

More chanel ex. stdout, stderr


date | echo "this"

date pass to stdin channel but not to pipe 


| only work when receive command  from first parameter


Interview Questions:

awk:pattern scanning and processing language

grep->return entire string
ps -ef | grep amazon
ubuntu    421823  396065  0 03:45 pts/1    00:00:00 grep --color=auto amazon

but awk command return specific column
ps -ef | grep amazon | awk -F " " '{print $2}'

set -e # exit the script when there is an error
set -o pipefail(check pipe faileure


Same command:

#set exo   pipefail

curl or wget
curl->transfoer file and 

wget ->download or store then apply fitler


Most popular command:

Find cmd for devops


sudo su - -> take root user
sudu manoj -> user




========Write a srcipt to report the usage of AWS in your project?===

aws_report_report.sh

#!/bin/bash

### Author: Manoj
### Date: 06/05/2025
### Purpose: List S3 bucket, list IAM users, list ec2 instances, list 

set -x
#List s3 bucket:

aws list s3>report.txt

# aws IAM users
 aws list-users>>report.txt
# aws ec instaces:

aws describe-instances>>report.txt


==================Video=====

aws cli or python boto3




Demo for schelling scripting:

Aws service report list 
git 
  

============Common shell scripting automation by devops Engineers====










===============Networking Abhisheck==================


 


 



=============Linux====
Bhupender Sir:



=======================Docker projects-m-prashant===================
====Docker is essentaill skills for Software engineer, Devops ===
Start learn it and apply in your project



docker ps
docker images or docker image ls
docker build . or docker build -t dockerhellotest/mini-app:v1 .
docker run -it image id or image name
docker run -it -p 3000:3000 dockerhellotest/mini-app:v1 
docker run  -d -p 3000:3000  dockerhellotest/mini-app:v1 
docker ps -a (all)
docker rm objective_meninsky
docker stop objective_meninsky
docker start objective_meninsky
docker run -d(detach) --rm(remove when stop)  -p 3000:3000 a5d2965c6bd5

docker run -d --rm --name "myapp" -p 3000:3000 a5d2965c6bd5 
docker rmi dockerhellotest/myapp:v1
docker push  dockerhellotest/front-react-app:v1 
#Rename
 docker tag myapp:v2  dockerhellotest/front-react-app:v1 
 
# Docker volume:
docker run -it --rm -v myvolume:/myapp/  dockerhellotest/front-react-app:v1 
#Mount with external services


#help docker other options:
 docker volume --help
 
 docker volume ls
 docker volume inspect myvolume
 
# Docker ignore
.dockerignore 
 
# External Call api

# Container interact with external db or other service
  python application with local db
# contact or communicate one container with another container

 docker run -d --env MYSQL_ROOT_PASSWORD="root" --env MYSQL_DATABASE="userinfo"  --name mysqldb mysql
 
# Docker network

 
docker network create my-net
docker run -it --rm --network my-net 3c1944d53232

# Docker compose

A config file to make your task of managing and runnning containers easy.
Get rid of repetive commands

all the services inside the config file, share some network

Commands:
docker-compose up/down
 -d detach mode
 -v to remove networks/volumes upon stop
 -- build to again build image and run


Configuration file to manage multiple containers running on same machine.
But also for single container

docker-compose.yml
services: container

docker-compose.yml
services:
   image: "image-namge"


>docker-compose up
> docker-compose down
       
Run single application:
docker-compose run -d mysqldb
docker-compose run -d myphythonapp
docker-compose run myphythonapp

if docker compose use, all services by default network use, 
create automatically network

docker compose down->only container down but network and volume persitent
docker compose down -v ->all down
 
 volumes:
      - ./servers.txt(relative path):/myapp/servers.txt(container file url)


Network:



========Commands======
servie docker status
docker info
Docker Engine or docker daemon
service docker start
service docker stop
docker run -it ubuntu /bin/bash
or
docker run -i -t ubuntu /bin/bash
docker search ubuntu
docker run -it --name manoj ubuntu /bin/bash
docker diff manoj updateimage
Docker commit manoj updateimage


FROM:->Mandatory
RUN->Linux COmmend
COPY->Copy from local
ADD ->from internet or zip->unzip
CMD->start program
ENTRYPOINT:-> 
ENV
ARG:
WORKDIR


CTRL+L->exit


#Docker volume:
VOLUME [ "/myvolume" ]
docker run -it --name container2 myimage-demo-vol /bin/bash
docker run -it --name container3  --privileged=true  --volumes-from container2 ubuntu /bin/bash
docker run -it --name container2 -v /volume2 ubuntu /bin/bash


Share host to container

docker volume ls
docker volume create v1
docker volume rm v1
docker volume prune(It remove all unused docker volume)
docker container inspect container1


docker run -it --name hostcont -v ./docker-volume:/manoj --privileged-true ubuntu /bin/dash

Docker port expose
logical port:
0-65535 ->transport layer


docker attach container1->go inside container and main process
docker exec -it contaner1 /bin/bash->inside container but create new process
docker run -td(daemon) myimage-vol
docker exec->new process enviroemnet or pid create
docker attach ->already running process open not new process 


Docker Engine: 28 version
As of May 2025, the latest stable version of Docker Engine is 28.1.1, released on April 18, 2025.



dockr port container1



# How to stop all running cotainers:
 docker stop $(docker ps -a -q)

# delete all stopped containers

docker rm $(docker ps -a -q)

#Delete all images:
docker rmi -f $(docker images -q)

 # how to push image on docker hub
 
 docker commit imagename image1
 docker tag image1 user1/project1
 docker push user1/project1
 
==================k8s -bhupendar=======


Declerative: write yml file
Imperative: write cmd or ternminal

Pods:
ReplicateSet: 
ReplicationController
jobs:
deployment
Cron jobs:
init container:




========================k8s-m-prashant====


====================Virtualization===
vm1|vm2|vm3
Host OS
Bare Metal
H/W


Hyperviser two types:

type-1 hyberversier-Enterprise              type-2 hyperviser->dummy for learning purpose


vm1|vm2|vm3                                     vm1|vm2|vm3 
Host OS                                            hperviser                        
Bare Metal                                         Host OS                                 
											    Bare Metal
												H/W			

 
H/W virtualization                                OS virtualization

operation:Guest OS and app. hyper.                   Run as app. on the host os



=========================docker-Abhisheck====







	

 
 
  
 
				  
				  
				  
	  
  
												 
    
          
  
   
   
