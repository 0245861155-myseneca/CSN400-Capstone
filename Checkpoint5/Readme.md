- **COURSE INFORMATION: CSN 400 NBB**
- **STUDENT’S NAME: Tyler Kirkwood**
- **STUDENT'S NUMBER: 024861155**
- **GITHUB USER ID: 0245861155-myseneca**
- **TEACHER’S NAME: Atoosa Nasiri**

# Part A

## Question 1: If you run docker build -t getting-started . for a second time, the build time will be different from first time, why? Why the number of steps are also different? Explain  your answers in detail.

### Docker build cache: Docker uses a layer-based caching mechanism during the build process. When you build an image, each step in the Dockerfile generates a new layer. If the previous layers remain unchanged, Docker can reuse them from the cache, saving time. However, if any of the previous steps change, Docker needs to rebuild those steps and all the subsequent steps, resulting in a longer build time.

### Build context changes: The in the command docker build -t getting-started represents the build context. It includes the files and directories in the current directory that are sent to the Docker daemon for building the image. If any files within the build context have changed since the previous build, Docker will need to reprocess those files, leading to a longer build time.
<br />

## Question 2: What does -t flag do? If you do not use it what is the error? embed the error in your answer.

```
ERROR: "docker buildx build" requires exactly 1 argument.
See 'docker buildx build --help'.

Usage:  docker buildx build [OPTIONS] PATH | URL | -

Start a build
```

### the error asks for exaclty 1 argument 
<br />

## question 3: Run docker build -t getting-started . a few times and then run docker image ls to get the list of your images, why do you still one image listed even though you have tried building image many times?

### because simply using the command many time without making sure its in a different space in the computer the image will always be in the same place continuously overwriting the same image.
<br />

## Question 4: What are -d and -p flags? What does each flag do? Start another git bah or wsl terminal and run docker run -p 1000:3000 getting-startedin it, Notice that -d is missing. What is the output?Embed it in your submission. Explain why this happened?

### the -p flag is used to publish container ports to host it specifies the port it will use like `docker run -p 1000:3000 getting-started` it shows what port range it will use
```
2023/06/09 12:20:27 [notice] 1#1: using the "epoll" event method
2023/06/09 12:20:27 [notice] 1#1: nginx/1.25.0
2023/06/09 12:20:27 [notice] 1#1: built by gcc 12.2.1 20220924 (Alpine 12.2.1_git20220924-r4)
2023/06/09 12:20:27 [notice] 1#1: OS: Linux 5.10.102.1-microsoft-standard-WSL2
2023/06/09 12:20:27 [notice] 1#1: getrlimit(RLIMIT_NOFILE): 1048576:1048576
2023/06/09 12:20:27 [notice] 1#1: start worker processes
2023/06/09 12:20:27 [notice] 1#1: start worker process 30
2023/06/09 12:20:27 [notice] 1#1: start worker process 31
2023/06/09 12:20:27 [notice] 1#1: start worker process 32
2023/06/09 12:20:27 [notice] 1#1: start worker process 33
2023/06/09 12:20:27 [notice] 1#1: start worker process 34
2023/06/09 12:20:27 [notice] 1#1: start worker process 35
2023/06/09 12:20:27 [notice] 1#1: start worker process 36
2023/06/09 12:20:27 [notice] 1#1: start worker process 37
2023/06/09 12:20:27 [notice] 1#1: start worker process 38
2023/06/09 12:20:27 [notice] 1#1: start worker process 39
2023/06/09 12:20:27 [notice] 1#1: start worker process 40
2023/06/09 12:20:27 [notice] 1#1: start worker process 41
2023/06/09 12:20:27 [notice] 1#1: start worker process 42
2023/06/09 12:20:27 [notice] 1#1: start worker process 43
2023/06/09 12:20:27 [notice] 1#1: start worker process 44
2023/06/09 12:20:27 [notice] 1#1: start worker process 45
```
### The reason the output is displayed directly in the terminal when the -d flag is missing is that the container is not running in detached mode. Without the -d flag, the container's output is attached to the current terminal session, allowing you to see the logs and interact with the container.

<br />

##  Question 5: The previous question has created a new container with your app running in it. Which port in localhost must be used to reach it?

### In the previous question, the container was running the application, and the specified port mapping was -p 1000:3000. Therefore, to reach the application running inside the container, you would need to use localhost:1000 in your web browser or any other client. Port 1000 on the localhost is mapped to port 3000 inside the container, allowing the traffic to be redirected correctly.

<br />

## Question 6: Run `docker ps` and embed the output in your answer. If you have completed previous questions, you should have at least two containers running in your system. What is their difference? Can you explain how and why this was necessary?

```
CONTAINER ID   IMAGE             COMMAND                  CREATED          STATUS          PORTS                            NAMES
139955dfc068   getting-started   "/docker-entrypoint.…"   39 seconds ago   Up 38 seconds   80/tcp, 0.0.0.0:1000->3000/tcp   dreamy_tu
```

### I only have one that is started
### however I can imagin the difference being the name is different, the container ID would be different because those are nessesary differenence
<br />

#
