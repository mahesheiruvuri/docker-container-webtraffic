# docker-container-webtraffic

Step1:	Create a Network  
          eg: docker network create webtraffic-network
        
step2:	start redis and attach to the above created network. 
          eg: docker run -it -p 6379:6379 --name myredis --network webtraffic-network redis
        
step3: 	update application index.js file with redis container port name and ip details.

step4:  create a Dockerfile 

step5: 	Build web application docker image 
          eg: docker build -t webtrafficapp .
        
step6:	run webtraffic container and attach to the created network. 
          eg: docker run -it -p 9999:9999 --name webtraffic-network webtrafficapp
	
