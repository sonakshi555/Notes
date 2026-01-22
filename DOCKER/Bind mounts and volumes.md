Main 3 problems in Docker

-  Scenario 1 : if the container goes down , then the application in container won't work and **all the log files in nginx is also deleted . No log records for  auditing is available**
 -  Scenario 2 : consider frontend and backend are containerized , and the user requests through frontend is sent to backend . Backend sends response in html / xml , yaml or json. **If the backend goes down , then previous details are lost .**
-  Scenario 3 : App in container, whose job is to read a file , that is provided by cron job on host. 
> **The file in the host cannot be accessed by container** , but can use resources like RAM, CPU and other stuffs

# To overcome this problem Bind mounts or Volumes is used

## Bind mounts :
 - It allows to bind a directory inside your container through the Host
 - Example : /app folder is binded to container through the Host
   Whatever the files written in /app folder can be accessed by container and vice versa
   means the files written by container is also accessible by Host ,even if container goes down
 - the same /app folder can be even binded to other container too
 
## Volumes : ==Used more==
-  does same thing as bind mount , but offers better lifecycle
- Using docker CLI , volumes can be created
- volume : logical partition created on the host ==> can be created or destroyed. 
- The volume from the one container can be attached to another container 
- A volume can be attached to both
- Advantage : No need of providing specific folder details 
- It has a lifecycle consists of creating ,managing and destroying it
- This volume can be create it on external sources

Docker volume creation can be done as follows
docker -v <arguments>
docker --mount 

docker volume create <volume_name> 
docker volume inspect <volume_name> 
	provides details about the volume like where it is created , when it is created and more
docker volume rm <volume_name>

if -v  : provide all the options such as src , dest , permission in one single line
if --mount : it is more verbose. It is easy to understand the detalis of the src permisson and all in detail steps


both does same work


Nginx is used primarily as a high-performance web server, reverse proxy, load balancer, and HTTP cache to efficiently handle large traffic volumes, improve website speed, and distribute requests across multiple backend servers, making applications faster, more reliable, and scalable for demanding sites like Netflix and Dropbox. It excels at managing connections, serving static content, terminating SSL, and acting as an intermediary for emails and other protocols.