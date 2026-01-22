networking allows container to communicate each other and host

### Scenario 1 : two container communicate each other
  >example : Frontend container and backend container
  >here both should communicate each other 

### Scenario 2 : two container should be isolated
>example : payment container and login container
>here they both need to be isolated

All container or host have eth0 , through which they can communicate with other
1. Bridge networking : host communicate to container through veth0 (virtual eth0 that is docker0) , virtual ethernet which is default. Both host and container have eth0 but not able to ping , so they use veth0 to ping. Without veth0 container cannot talk to Host and become not reachable through internet
2. Host networking : Container will directly use the host means the container use the subnet of the host . If the access to host is allowed then the access to container is also used , which is vulnerable to cyber attaks
3. Overlay networking : used in container orchestration. A situation where the containers are running in multiple host . Inorder to create the cluster of those Host together ,this networking is used.
4. macvlan : Allow container to appear as physical host rather than a container. This advanced driver allows you to assign a MAC address to a container, making it appear as a physical device on your network. This is useful for integrating with legacy applications or network monitoring tools that expect devices to have a physical network presence.
# Scenario 1 : 
this can be achieved by using custom bridge networking
### Out Of The Box (OOTB) Bridge network:
usually 2 container using same host uses same veth0 , which is vulnerable
and it is called OOTB.

A custom bridge can be used to overcome default bridge network





https://www.geeksforgeeks.org/devops/basics-of-docker-networking/