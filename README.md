# Aize-spring-boot-EoinGordon
Project for Aize interview process

##Spring Boot Api docker image instructions

To pull docker image down to host machine, run docker pull eoinjag/aizespringboot

Alternatively, access this link "https://hub.docker.com/r/eoinjag/aizespringboot" and copy the command listed. 

Once docker image has finished pulling, you can use command: docker run -it eoinjag/aizespringboot

Next, we are going to run docker exec to pass in some commands to the container, so it can run detached. 
Before we do this we will need to use "docker ps" to get a list of container ID's

![image](https://user-images.githubusercontent.com/46785081/173076357-95343b9e-afa0-4844-8a9d-ae0e23fe5eea.png)


The exec command should now be input: docker exec -it -d <container id> /bin/bash -c "cd /spring-boot-projects/spring-boot-modules/spring-boot-angular/; mvn spring-boot:run"
  
  ##Angular front end docker image instructions
  
  To pull docker image down to host machine, run docker pull eoinjag/aizeangular
  
  Alternatively, access this link "https://hub.docker.com/r/eoinjag/aizeangular" and copy the command listed.
  
  Once docker image has finished pulling, you can use command: docker run -it -p 4200:4200 eoinjag/aizeangular
  
  When in the docker image, you can run command "cd /spring-boot-projects/spring-boot-modules/spring-boot-angular/src/main/js/application" to change to the correct     directory, from here you can run the command ng serve & the front end should run. 
