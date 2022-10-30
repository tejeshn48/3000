# DOCKER
Docker is open-source software for building, shipping, managing, and securing containers.
Docker has started its life as a platform as a service provider called dot cloud. The dot cloud platform leveraged Linux containers. To help them create and manage these containers they built an internal tool that they named DOCKER.
That is how Docker entered the Information and Technology

##### Why Is Docker? 
The developer is blind to the code and the code is working fine and sent to Tester but the same code is don’t work on the Tester system, The code doesn’t work on another system due to the difference in computer environments. So, what could be the solution to this problem?
###### Virtual Machine can be the solution and Docker will be a better solution
What is the main difference between Virtual Machine and Docker
1.	Docker is more light than Virtual Machine but provides the same functionality
2.	virtual machine occupies a lot more memory space on the host machine
3.	Docker just boots up faster the performance of the Docker environment is better and more consistent than the virtual machine 
4.	Docker is also very easy to set up and very easy to scale the efficiencies, therefore a much higher with a Docker environment versus a virtual machine environment
5.	Docker finds it is easier to port Docker across multiple platforms than a virtual machine finally the space allocation between Docker and Virtual Machine is significant, etc.

There are many reasons Docker will be a better solution than the Virtual Machine
Docker resources 
1.	Docker homepage 
2.	 Docker Hub 
3.	 Docker blog

## Requirements
Requirements For all of these installation types, Docker has some basic prerequisites. 
To use Docker you must requirements and configuration :
1.	Be running a 64-bit architecture. 32-bit is currently supported. 
2.	 Be running a Linux 3.8 or later kernel. Some earlier kernels from 2.6.x and later will run Docker successfully. Your results will greatly vary, though, and if you need support you will often be asked to run on a more recent Installing kernel.

## Installation Docker
Docker can be installed in window OS, mac OS, and Linux OS. we will install Docker on Ubuntu 16.04 server in this 
Document. Docker can be installed directly from the Ubuntu repo but that may not be the latest version of the Docker engine. To install the latest version, we are installing it from the official Docker repository  
 
Add GPG key for Docker repository
~~~
https://download.docker.com/linux/ubuntu/gpg|sudo apt-key add-
~~~
 Add the Docker repository
 ~~~
https://download.docker.com/linux/ubuntu $(lsb_release-cs) stable”
~~~
### Updates the package
~~~
Sudo apt-get updates
~~~
## Install Docker
~~~
Sudo apt-get Install docker-ec -y
~~~
Docker should be installed, the demon started, and the process enabled to start on boot. Check that it’s running
~~~
Sudo systemctl status docker
~~~
  
Docker commands can be executed by root user or by providing sudo. We can run the Docker command with a normal user in the docker group.
~~~
Sudo usermod –aG docker<’ username>
~~~
You need to log out and log in to reflect the changes.

Run the Docker command to check if it’s working.
~~~
docker --version
~~~

When you install Docker-engine you get two components
1. Docker client
2. Docker Engine
## DockerImage
Images are the building blocks of the Docker world. You launch your containers from images. Images are the "build" part of Docker's life cycle. They are a layered format, using Union file systems, that are built step-by-step using a series of instructions. 
Let's continue our journey with Docker by learning a bit more about Docker images. A Docker image is made up of filesystems layered over each other. At the
base is a boot filesystem, bootfs, which resembles the typical Linux/Unix boot
filesystem. A Docker user will probably never interact with the boot filesystem.
Indeed, when a container has booted, it is moved into memory, and the boot
filesystem is unmounted to free up the RAM used by the initrd disk image.
So far this looks pretty much like a typical Linux virtualization stack. Indeed,
Docker next layers a root filesystem, rootfs, on top of the boot filesystem. This
rootfs can be one or more operating systems
Images and stopped state of containers. Run the docker images command.
~~~
$ docker images
~~~
This command will list the download image on your machine, so you won’t see anything now in the output. We need to download some images, in the Docker world we call it pulling an image. So where does it pull the image from? Again, same analogy as vagrant boxes. we download the vagrant boxes from the vagrant cloud, Docker images are downloaded from Docker registries, the most famous docker registry is DockerHub. There are other registries as well, from google, RedHat, etc.
~~~
$ docker pull Ubuntu: latest
Latest: Pulling from library/Ubuntu
bd97b43c27e3:pull complete
6960dc1aba18: pull complete
2b61829b0db5: pull complete
1f88dc826b14: pull complete
73b3859b1e43: pull complete
~~~
Digest:
Status: Downloaded newer image for Ubuntu: latest
Run the docker image command again to see the Ubuntu: latest image you just pulled



For example: 
1.	Add a file. 
2.	Run a comma
3.	Open a port. 
You can consider images to be the "source code" for your containers. They are highly portable and can be shared, stored, and updated. In the book, we'll learn how to use existing images as well as build our images.
## Docker Desktop
Docker helps you build and deploy containers inside which you can package your applications and services. As we've just learned, containers are launched from images and can contain one or more running processes. You can think about images as the building or packing aspect of Docker and the containers as the running or execution aspect of Docker.
## Container
 A Docker container is: 
1.	An image format. 
2.	 A set of standard operations. 
3.	 An execution environment.
 Docker borrows the concept of the standard shipping container, used to transport goods globally, as a model for its containers. But instead of shipping goods, Docker containers ship software
Now that we have an image pulled locally on our Docker host, we can use the Docker run command to launch a container from it.
Look closely at the output from the command above. you should notice that your shell prompt has changed. This is because your shell is now attached to the shell of the new container you are literally inside of the new container, let’s examine that docker run command.
1.	Docker run tells the docker daemon to start a new container.
2.	The it flags tell the daemon to make the container interaction and to attach our current shell to the shell of the container.
3.	Next, the command tells Docker that we want the container to be used on the Ubuntu: latest images.
4.	We tell it to run the /bin/bash process inside the container.
Run the following ps command from inside of the container to list all running processes
As you can see from the output of the ps command, these are only two processes 
## Running inside the container:
1.	PID 1. This is the /bin/bash process that we told the container to run with the docker run command.
2.	PID 0 . this is the ps- elf process that we ran to list running processes.
The presence of the ps – elf process in the output above could be a bit misleading as it is a short-lived process that dies as soon as the ps command exits. This means that the only long-running process inside the containers is the /bin/bash process. Press
Ctrl-PQ to exit the container. This will land you back in the shell of your Docker host. You can verify this by looking at
You can verify this by looking at your shell prompt. in a previous step, you pressed Ctrl PQ to exit your shell from the container. Doing this from inside of a container will exit you from the container without killing it. you can see all the runnings containers on your system using the docker ps command
~~~
Ravi@DEvOps:~S docker ps
CONTAINER ID IMAGE COMMAND CREATED STATUS
PORTS NAMES
B8765d3a67a9 ubuntu: latest “/bin/bash” 6 minutes ago Up 6 minutes 
Inspiring_heyrovsky
~~~
The output above shows a single running container .this is the container that you created earlier. The presence of your container in this output proves that it’s still running. you can also see that it was created 6 minutes ago and has been running for 6 minter
## Connecting to the Redis
 container Let's now update our Sinatra application to connect to Redis and store our incom ing parameters. In order to do that, we're going to need to be able to talk to the Redis server. There are several ways we could do this; let's explore and see the pros and cons of each. The first method involves Docker's own network stack. So far, we've seen Docker containers exposing ports and binding interfaces so that container services are exposed on the local Docker host's external network.In addition to this capability, Docker
has a facet we haven't yet seen: internal networking.
Every Docker container is assigned an IP address, provided through an interface
created when we installed Docker. That interface is called docker0. Let's look at
that interface on our Docker host now.

## Docker Registries
Docker images are stored in image registries. The most command image registry is Docker Hub. Other registries exit
Including 3rd praty registries and secure on-premises registries, but Docker Hub is the default, and it’s the one we’ll use in this document.
~~~
https://hub.docker.com/
~~~


docker hub contains official and unofficial repositories. Official repositories are from Docker, including. these are safe and secure images with the latest up-to-date software.
The unofficial repo is uploaded by anyone and is not verified by Docker. The list below contains a few of the official repo and shows their URLs that exit at the top level of the docker hub namespace:
~~~
1. nginx – https://hub.docker.com/_/nginx/
2. busybox– https://hub.docker.com/_/nginx/busybox/
3. redis – https://hub.docker.com/_/redis/
4. mongo - https://hub.docker.com/_/mongo/
~~~

## Attaching to Running containers
You can attach your shell to running containers with the docker exec command. As the container from the previous steps is still running let’s connect back to it.
The example below references a container called “inspiring_heyrovsky”. the name of your container will be different, so remember to substitute
“inspiring_heyrovsky” with the name or ID of the container running on your Docker host.
~~~
Ravi@DevOPs:~$ docker exec –it inspiring_heyrovsky/bin/bash
Root@b8765d3a67a9:/#
~~~
That your shell prompt has changed again. You are back inside the container.
The format of the docker exec command is 
~~~
Docker exec –options<’container-name or container-id<’ command>.
~~~
In our example, we used the –it options to attach our shell to the container’s shell. We referenced the container by name and told it to run the bash shell.
Exit the container again by pressing Ctrl-PQ.
Your shell prompt should be back to your Docker host.
Run the docker ps command again to verify that your container is still running.
### Building and shipping Images
Docker can build images automatically by reading the instructions from a Dockerfile, a text file that contains all the commands, in order, needed to build a given image. Dockerfile adheres to a specific format and uses a specific set of instructions. Dockerfile will define what goes on in the environment inside your container. Access to resources like networking interfaces and disk drives is virtualized inside this environment, which is isolated from the rest of your system, so you have to map ports to the outside world, and be specific about what files you want to “copy in ” to that environment. However, after doing that, you can expect that the build of your app Defined in this Dockerfile will behave the same wherever it runs.

#### Running a Consul cluster in Docker 
As Consul is distributed we'd normally create three hosts to run in separate data centers, clouds, or regions. Or even add an agent to every application server. This will provide us with sufficient distributed resilience. We're going to mimic this required distribution by creating three hosts each with a Docker daemon to run Consul. We've created three new Ubuntu 14.04 
~~~
$ sodu docker pull jamtur01/consul
~~~
On each host, we're going to run a Docker container with the jamtur01/consul image. To do this we need to choose a network to run Consul over. In most cases, this would be a private network, but as we're just simulating a Consul cluster, I will use each host's public interface. To start Consul on this public network I will need each host’s public IP address. This is the address we're going to bind each Consul agent too


# Asyncio
Asyncio deals with three create functions of python async programming 
1.	The first function is the event loop that leads to managing the asynchronous result and distributes then to execute the program.
2.	The coroutines are functions that maintain time-lapse in the execution of events.
3.	Futures are the result of the Execution of the coroutine. 
The main functions are in python
1.	Asyncio is a package that comes with python that gives an API to run and manage coroutines.
2.	Async/await is used to run defined coroutines in the program.
Asyncio is used for
See with example program
~~~
Import asyncio
Async def hello():
Print(“Ravi chandra”)
await asyncio.sleep(3)
print(“ravi chandra”)
    asyncio.run(hello())
~~~
output
~~~
Ravi Chandra
Ravi chandra
~~~


Think that this is a synchronous code because the second print is waiting 3 seconds to print “Ravi chandra” after “ravi chandra”. But this code is actually asynchronous.
## Coroutine
The function explained as an async def keyword is a coroutine same as a function name and calling the function name is not the same as the cover inside asyncio.run() function
1.	asyncio.run() function accessing the complete functionality of the async program that starts the event loop and executes the coroutine.
2.	await to await function is taken to the coroutine and passes the control to the ## Event loop.
~~~
import asyncio
import time
async def say_something(delay, words):
    print(f"Before {words}")
    await asyncio.sleep(delay)
    print(f"After {words}")
async def main():
    print(f"Started: {time.strftime('%X')}")
    await say_something(1, "Task 1")
    await say_something(2, "Task 2")
    print(f"Finished: {time.strftime('%X')}")
asyncio.run(main())
~~~
output
~~~
Started: 15:59:52
Before Task 1
After Task 1
Before Task 2
After Task 2
Finished: 15:59:55
~~~

The say_something() coroutine to finish so it executes task 1 in 1 second, and then executes the second task after waiting for 2 seconds.

Its make the coroutine run concurrently, we should create tasks which is the third process.

###### asyncio.create_task() function 
~~~
example program:
import asyncio
import time
async def say_something(delay, words):
    print(f"Before {words}")
    await asyncio.sleep(delay)
    print(f"After {words}")
async def main():
    print(f"Started: {time.strftime('%X')}")
    task1 = asyncio.create_task(say_something(1, "Task 1"))
    task2 = asyncio.create_task(say_something(2, "Task 2"))
    await task1
    await task2
    print(f"Finished: {time.strftime('%X')}")
asyncio.run(main())
~~~
output
~~~
Started: 16:07:35
Before Task 1
Before Task 2
After Task 1
After Task 2
Finished: 16:07:37
~~~
The above code is now running concurrently and the say_something() coroutine is no longer waiting for the say_something() coroutine to finish. It's rather running the same coroutine with different parameters concurrently
example:
###### concurrent tasks with asyncio.gather()
~~~
import asyncio
import time
async def greetings():
    print("Welcome")
    await asyncio.sleep(1)
    print("Goodbye")
async def main():
    start = time.time()
    await asyncio.gather(greetings(), greetings())
    elapsed = time.time() - start
    print(f"{__name__} executed in {elapsed:0.2f} seconds.")
asyncio.run(main())
~~~
output
~~~
Welcome
Welcome
Goodbye
Goodbye
~~~
__main__ executed in 1.00 seconds.with
In the previous code, the greetings() coroutine is executed twice concurrently.

## Coroutines
example:
###### coroutines, tasks, and futures.
~~~
import asyncio
async def mult(first, second):
    print("Calculating multiplication...")
    await asyncio.sleep(1)
    mul = first * second
    print(f"{first} multiplied by {second} is {mul}")
    return mul
async def add(first, second):
    print("Calculating sum...")
    await asyncio.sleep(1)
    sum = first + second
    print(f"Sum of {first} and {second} is {sum}")
    return sum
async def main(first, second):
    await mult(first, second)
    await add(first, second)
asyncio.run(main(10, 20))
~~~
output
~~~
Calculating multiplication...
10 multiplied by 20 is 200
Calculating sum...
Sum of 10 and 20 is 30
~~~
In the previous example, the mult() and add() coroutine functions are awaited by the main() coroutine.
## Tasks
To schedule a coroutine to run in the event loop, we use the asyncio.create_task() function.
example
~~~
import asyncio
async def mult(first, second):
    print("Calculating multiplication...")
    await asyncio.sleep(1)
    mul = first * second
    print(f"{first} multiplied by {second} is {mul}")
    return mul
async def add(first, second):
    print("Calculating sum...")
    await asyncio.sleep(1)
    sum = first + second
    print(f"Sum of {first} and {second} is {sum}")
    return sum
async def main(first, second):
    mult_task = asyncio.create_task(mult(first, second))
    add_task = asyncio.create_task(add(first, second))
    await mult_task
    await add_task
asyncio.run(main(10, 20))
~~~
output
~~~
Calculating multiplication...
Calculating sum...
10 multiplied by 20 is 200
Sum of 10 and 20 is 30
~~~
## Futures
A Future is a low-level awaitable object that represents the result of an asynchronous computation. It is created by calling the asyncio.Future() function.
~~~
from asyncio import Future
future = Future()
print(future.done())
print(future.cancelled())
future.cancel()
print(future.done())
print(future.cancelled())
~~~
output
~~~
False
False
True
True
~~~
## Timeouts
~~~
import asyncio
async def slow_operation():
    await asyncio.sleep(400)
    print("Completed.")
async def main():
    try:
        await asyncio.wait_for(slow_operation(), timeout=1.0)
    except asyncio.TimeoutError:
        print("Timed out!")
asyncio.run(main())
~~~
# Timed out!
The timeout here in the Future object is set to 1 second although the slow_operation() coroutine is taking 400 seconds to complete.
example:
###### asyncio.TimeoutError
~~~
import asyncio
async def slow_operation():
    await asyncio.sleep(400)
    print("Completed.")
async def main():
    try:
        await asyncio.wait_for(slow_operation(), timeout=1.0)
    except asyncio.TimeoutError:
        print("Timed out!")
asyncio.run(main())
~~~
# Timed out!
The timeout here in the Future object is set to 1 second although the slow_operation() coroutine is taking 400 seconds to complete.
## conclusion
The function of asynchronous programming using the Python asyncio module. The asyncio gives us programmatic execution of when block of code when we use the context switches. That means we can managing many complex methods that occur with concurred in programming.









