
**Title: Introduction to Docker**

### 1. Introduction
**Objective**: Understand the basic ***principles*** of Docker and how it can be used to create, deploy, and run applications in ***containers***.

**Importance**: Docker is a widely used platform that allows the creation of isolated ***environments*** for running applications, ensuring consistency and portability.

### 2. Main Content
#### 2.1. Theory and Concepts
**What is Docker?**
- Docker is a container platform that allows developers to package, distribute, and run any application anywhere.

**Key Concepts**:
- **Docker Image**: An ***immutable*** template that contains everything needed to run an application (code, runtime, libraries, etc.).
- **Docker Container**: A running ***instance*** of a Docker image. It can be thought of as a running application.
- **Dockerfile**: A script that contains a collection of instructions for creating a Docker image.
- **Docker Hub**: An image registry where Docker images can be stored and shared.

#### 2.2. Practical Examples
**Example 1: Running a Simple Docker Container**
- Command to run a simple container:
  ```sh
  docker run hello-world
  ```

**Example 2: Creating a Docker Image**
- Create a `Dockerfile` for a Node.js application:
  ```Dockerfile
  # Use an official Node.js base image
  FROM node:14

  # Set the working directory
  WORKDIR /app

  # Copy package files
  COPY package*.json ./

  # Install dependencies
  RUN npm install

  # Copy the rest of the application code
  COPY . .

  # Expose the port the app runs on
  EXPOSE 3000

  # Command to run the application
  CMD ["node", "app.js"]
  ```

- Build the Docker image:
  ```sh
  docker build -t my-node-app .
  ```

- Run the Docker container:
  ```sh
  docker run -p 3000:3000 my-node-app
  ```

#### 2.3. Activities
- **Quiz**: Define the key concepts of Docker (image, container, Dockerfile, Docker Hub).
- **Exercise**: Write a Dockerfile for a simple code application and build the Docker image.

#### 2.4. Additional Resources
- [Docker Documentation](https://docs.docker.com)
- [Docker Hub](https://hub.docker.com)
- [Docker Cheat Sheet](https://dockerlabs.collabnix.com/docker/cheatsheet/)

### 3. Conclusion
**Summary**: Docker simplifies the process of developing, deploying, and running applications by using containerization technology. Understanding the basics of Docker can significantly improve development workflows.

**Next Steps**: Implement a Dockerfile for your own project and run it in a container.

### 4. Appendix
**Glossary of Terms**:
- **Container**: A lightweight, standalone, executable package of software.
- **Image**: A read-only template with instructions for creating a Docker container.
- **Dockerfile**: A text file that contains all the commands to assemble an image.
