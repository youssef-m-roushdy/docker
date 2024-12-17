# Introduction To Docker

<b>Docker:</b> is a set of platform as a service which is known as as PAAS products that use the operating system level visualization to deliver software in packages called containers. That is, the basic principle of Docker is build, ship, and run any software anywhere.

  * Docker is a tool designed to build, deploy, and run the application with ease by using containers
  * It allows a developer packaging of an application with all of the requirements.
    * Such as libraries and other dependancies and ship it all as one package
  * It ensures that your application works seamlessly in any environment (Development, Production or Test environment)

## Why Docker

  * The goal is to ease the creation, deploy and the delivery of an applicaction using the containers
  * Develope an app using Docker containers with any language and any toolchain
  * Scales to 1000s of nodes, move data between cloud and the centric iterations update with zero downtime
  * shipping the Dockerized apps and dependencies anywhere to QA, Teammates or the Cloud without breaking anything

## Benefits Of Using Docker

  * Enable Consistent Environment
  * Easy to use and maintain
  * Efficient use of system resources
  * Increase operational efficiency
  * Increases Developer Productivity

## Docker Principles

<img src="https://miro.medium.com/v2/resize:fit:1400/1*E8dSDBHVNSzj-yIRMwQtHQ.png" alt=""/>

# Docker Architecture

<img src="https://media.geeksforgeeks.org/wp-content/uploads/20221205115118/Architecture-of-Docker.png" alt=""/>

The Docker client talks with the Docker daemon, which helps in building, running, and distributing the Docker container. Docker client runs with the daemon on the same system. Or we can connect the Docker client with the Docker daemon remotely. With the help of REST API over a Unix socket or a network, the Docker client and the daemon can connect with each other. The question is, what is this Docker daemon exactly? Docker daemon basically helps in managing all the services by communicating with other daemons. It manages Docker objects such as the Docker images, containers, and volumes with the help of API request of the Docker. With the help of this Docker client, the Docker users can interact with the Docker. The Docker command uses the Docker API like Docker build, Docker pull, or Docker run. Docker client can communicate with multiple daemons. When a Docker client runs any Docker command, the Docker terminal sends instructions to the daemon about what you would like to access. Would you like to build image? Would you like to push or pull the image? Would you like to run your container or the ps? Or would you like to run your Docker image? The Docker daemon gets those instructions from the Docker client with inside the shape of the command and the REST API's request. 

The main objective of the Docker client is to provide the responsibility to the Docker host to run the container, and in one container will be running multiple images. The common commands which are used by the Docker clients, as I mentioned, build, pull, and run. That comes with a registry. All the Docker images are stored in the Docker registry. There is a public registry which is known as a Docker Hub, I will tell you how you can register yourself there, that can be used by anyone. We can run our private registry also and allow the people to access, but that is a paid version of the registry. With the help of Docker run and Docker pull command, we can pull the required images from our configured registry, and images are pushed into the configured registry with the help of the pull or push command. This is how the Docker architecture works. We do have a Docker storage, which is the active storage. We can store data within the writable layer of the container, but it requires a storage layer.

## Docker Daemon

الـ Docker Daemon (المعروف أيضًا بـ dockerd) هو العملية الرئيسية المسؤولة عن إدارة مكونات Docker وتشغيلها. يُطلق عليه أحيانًا بالعربية "الخفي" لأنه يعمل في خلفية النظام بدون تفاعل مباشر مع المستخدم.

سبب تسميته بـ "الخفي":
التشغيل في الخلفية:

مثل أي Daemon في أنظمة Unix/Linux، يعمل Docker Daemon كعملية خلفية (Background Process) دون ظهورها مباشرة للمستخدم.
دوره الأساسي:

يتولى Docker Daemon إدارة الحاويات (Containers) والصور (Images) والشبكات (Networks) والحجم (Volumes) وكل الموارد الأخرى الخاصة بـ Docker.
آلية العمل:

يتلقى Docker Daemon الأوامر من واجهة Docker CLI أو واجهة برمجية (API)، ثم يقوم بتنفيذها خلف الكواليس.
تشبيه بالـ "خفي":

في الأنظمة، يتم استخدام مصطلح Daemon للإشارة إلى العمليات التي تعمل بصمت في الخلفية لتقديم خدمات أو وظائف معينة، وهذا مشابه لكلمة "الخفي" في اللغة العربية.

## Docker For Developers

  * Developers can use Docker to create reproducible environments for their applications
  * They can package their code, dependancies, and configrations, into a container image and then destribute to others
  * This ensures that the application will run the same way across different environments
  * Such as development, testing, staging, and production
  * Docker provides developers with a powerful and flexible platform for building and running applications that can improve productivity reduce complexity and increase agility

## Docker Community VS Docker Enterprise

<table style="width: 50%; border-collapse: collapse; margin: 20px auto; min-width:600px">
    <thead>
        <tr>
            <th style="border: 1px solid #000; padding: 8px; text-align: center;">Docker Community</th>
            <th style="border: 1px solid #000; padding: 8px; text-align: center;">Docker Enterprise</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="border: 1px solid #000; padding: 8px; text-align: center;">For developers and small organizations</td>  
            <td style="border: 1px solid #000; padding: 8px; text-align: center;">For business and production apps</td>  
        </tr>
        <tr>
            <td style="border: 1px solid #000; padding: 8px; text-align: center;">It is free</td>
            <td style="border: 1px solid #000; padding: 8px; text-align: center;">It is a Subscrition model</td>
        </tr>
        <tr>
            <td style="border: 1px solid #000; padding: 8px; text-align: center;">Stable version (every 3 months)</td>
            <td style="border: 1px solid #000; padding: 8px; text-align: center;">Stable version (every 3 months)</td>
        </tr>
        <tr>
            <td style="border: 1px solid #000; padding: 8px; text-align: center;">Edge version (every month), with cutting edge features</td>
            <td style="border: 1px solid #000; padding: 8px; text-align: center;">Additional enterprise fatures (management, security etc)</td>
        </tr>
        <tr>
            <td style="border: 1px solid #000; padding: 8px; text-align: center;">Docker's CLI and API are used for create, buildand deploy application</td>
            <td style="border: 1px solid #000; padding: 8px; text-align: center;">Universal Control Plane is used for create, build and deploy application</td>
        </tr>
    </tbody>
</table>

## Docker Hub

  * It is a registry or a registry service on the Cloud that allow you to push or pull the Docker images that are official images built by other users or vendors
  * We can treat this as a Github, where we fetch and push our source code
  * But in the case of Docker Hub, we download or publish our container images
  * A Cloud-based repository for public and private images
  * Here, Docker users and partners create, test, store and distribute container images
  * Users can host and share thier own custom images
  * Once we have pushed our images successfully, with the help of a webhook, it triggers an action to integrate Docker Hub with other services

<img src="https://k21academy.com/wp-content/uploads/2021/03/Screenshot-from-2021-03-26-11-01-09.png" alt=""/>

## How To Publish Your Docker Image To Dockerhub

  * Create a docker repository
  * Login into your docker hub account: `docker login`
  * Create a tag name for your image you want to push `docker tag imageId Name:Tag`
  * Then push into that repository you just create d`ocker push youssef2004/hello-docker:HelloDocker`
