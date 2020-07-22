# sample-spring-rest-boot
1.check the version of docker on your machine: <br/>
docker -v <br/>
2. We are going to use this docker to deploy our jar into an image and we are going to start that image <br/>
3. In order to start the image we need to build our image: <br/>
3a. Go to the current directory of the project  <br/>
cd /Users/santoshnijalingappa/Documents/spring_workspace/sample-spring-rest-boot <br/>
3b. docker build -f DockerFile -t docker-sample-spring-boot . <br/>
3d. How to check if this image is built successfully <br/>
docker images <br/>
The above command will show all the docker images in my docker container present locally <br/>
3e. How to run this image <br/>
docker run -p 8085:8085 docker-sample-spring-boot <br/>
You are basically saying that you are going to push the application on to port 8085 and inside the container you have exposed 8085  <br/>
You are mapping the machine's 8085 port to the container's 8085 port <br/>
Also make sure that the server.port property value is set as 8085 in application.properties file of your spring boot app <br/>
3f. Check if Spring Boot app is running <br/>
http://localhost:8085/greeting <br/>
This should show "Hello World!" on the browser <br/>

This is how you deploy your Spring boot application to docker container and run the same on docker engine <br/>








