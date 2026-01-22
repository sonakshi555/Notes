 Docker file 
- add things that required for execution not for building related things

#### Multi stage build (MSB)
the docker file is broken into 2 stages as part of same docker file
- means have 2 **FROM** statement
Stage 1 : 
>Not providing the entry point in this stage ,instead the binary is taken from stage 1 to stage 2
>CMD is not added here

Stage 2 : 
>here we can find very minimal image
>Or  Distroless images
>Can copy the artifact binary
>COPY --FROm , using alias
>CMD [ / app ]

Example : 3 tier architecture 
- frontend : React -> JS
- Backend : Spring boot -> Java
- Machine Learning -> Python
We cannot choose Java or python as Runtime image , if we use it ,can go crazy with 1 GB to 1.5 GB
So in order to overcome this issue, use MSB
There can be multi stage but the final one will be minimalistic image
Stage 1 : Frontend
Stage 2 : Backend
**Final stage** : get the dependences from both the stages ,a as part of CMD we execute it

# Distroless images 
- By using distroless images , efficiency of the docker multi stage Docker can be maximized
- Very minimalistic and lightweight , that have only Runtime environment
- It provide security ,because before when we use Ubuntu and Python images , it had some vulnerabilities which was prone to Cyber attacks
- So to solve this we moved to distroless images , in which were we won't have the access to commands such as ls, cd shell commands
- Since GoLang is statiscally , it doesn't require runtime environment
- 