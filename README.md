# sample-spring-rest-boot
1.check the version of docker on your machine:
docker -v
2. We are going to use this docker to deploy our jar into an image and we are going to start that image
3. In order to start the image we need to build our image:
3a. Go to the current directory of the project 
cd /Users/santoshnijalingappa/Documents/spring_workspace/sample-spring-rest-boot
3b. docker build -f DockerFile -t docker-sample-spring-boot .
3d. How to check if this image is built successfully
docker images
The above command will show all the docker images in my docker container present locally
3e. How to run this image
docker run -p 8085:8085 docker-sample-spring-boot
You are basically saying that you are going to push the application on to port 8085 and inside the container you have exposed 8085
You are mapping the machine's 8085 port to the container's 8085 port
Also make sure that the server.port property value is set as 8085 in application.properties file of your spring boot app
3f. Check if Spring Boot app is running
http://localhost:8085/greeting
This should show "Hello World!" on the browser

This is how you deploy your Spring boot application to docker container and run the same on docker engine








