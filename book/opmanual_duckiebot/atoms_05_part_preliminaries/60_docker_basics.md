# Docker basics {#preliminaries-docker-basics status=draft}

Assigned: Aleks

Note: there is plenty of material around.

## What is Docker?

Docker is used to perform operating-system-level virtualization, something often referred to as containerization. While Docker is not the only software that does this, it is by far the most popular one. Containerization is a process that allows partitioning the hardware and the kernel of an operating systems in such a way that different 'containers' can co-exist independently from one-another on the same system. Programs running in such a container have access only to the resources they are given access to and are completely independent of libraries and configurations of the other containers and the host machine.

Containers are often compared to virtual machines (VMs). The main difference is that VMs require a host operating system (OS) with a hypervisor and a number of guest OS, each with their own libraries and application code. This can result in a significant overhead. Imagine running a simple Ubuntu server in a VM on Ubuntu: you will have most of the kernel libraries and binaries twice and a lot of the processes will be duplicated in the host OS and in the guest OS. Containerization, on the other hand, leverages the existing kernel and OS and adds only the additional binaries, libraries and code necessary to run a given application. See the illustration bellow.

<figure class="flow-subfigures">  
    <figcaption>Comparison between containers and VMs (from [docker.com](https://docs.docker.com/get-started/))</figcaption>
    <figure>
        <figcaption>Using containers</figcaption>
        <img style='width:20em' src="images/docker-containerVM.png"/>
    </figure>
    <figure>  
        <figcaption>Using VMs</figcaption>
        <img style='width:20em' src="images/docker-containerVM2.png"/>
    </figure>
</figure>  

Because containers don't need a separate OS to run they are much more lightweight than VMs. This makes them perfect to use in cases where one needs to deploy a lot of independent services on the same hardware or to deploy on not-especially powerful platforms, such as the Raspberry Pi Duckiebots use. Containers allow for reuse of resources and code, but are also very easy to work with in the context of version control. If one uses a VM, they would need to get into the VM and update all the code they are using there. With a Docker container, the same process is as easy as pulling the container image again.

## How does Docker work?




- technology behind it: layers, images, containers, API, deamon, CLI
- why using it for robotics: lightweight, continuous development, automatics builds, etc
- windows support


## Frequently-used commands

run
-itd
--volume
--port
--privileged
--device
docker socket


container rm, attach, start, stop,
image list, rm, pull, prune?, details?
system prune


## Further resources

More resources about Docker:
Docker official Get Started tutorial: https://docs.docker.com/get-started/
Docker Curriculum: https://docker-curriculum.com/
