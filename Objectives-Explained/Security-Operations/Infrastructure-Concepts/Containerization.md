# Containerization

## Explanation

Containerization is a kind of cousin to virtualization, containers are minimalist operating systems which run all the code necessary for a specific application on top of an existing infrastructure (this may be a dedicated hypervisor or regular operating system).  Most big PC video games are run within containers, because the developers have no way of knowing whether all of the game's dependencies exist on every user's device.  Containers also have backend functions, when an application is being run in the cloud, it may be most efficient just to package the minimum code needed in order for the application to run and place it onto the a virtual server.  Not to get too detailed, but when you run a big application for lots of people, eventually a single server (or container) isn't enough for everyone to get decent service, so you need to scale up; when you scale up, you don't want to pay for any more computing resources than are absolutely necessary, but you still need all the same code that made the app run in the first place- this is what containers accomplish.

## Importance

Containers are everywhere doing everything, their popularity continues to grow as they are a cheap means of achieving efficient, scaleable architecture; since they're everywhere and doing everything, if they're misconfigured then they're misconfigured everywhere and everything is at risk.

## Example

Docker is by far the most popular containerization platform, when combined with Kubernetes (an orchestration platform for controlling, monitoring, and scaling containers), you can achieve a balanced, scaleable virtual infrastructure.

## Resources

- [FreeCodeCamp - A Beginner-Friendly Introduction to Containers, VMs and Docker](https://www.freecodecamp.org/news/a-beginner-friendly-introduction-to-containers-vms-and-docker-79a9e3e119b/)
- [Docker - Use containers to Build, Share and Run your applications](https://www.docker.com/resources/what-container/)
- [Google Cloud - What are Containers?](https://cloud.google.com/learn/what-are-containers)
- [NetApp - What are containers?](https://www.netapp.com/devops-solutions/what-are-containers/)