# Project 5

## Part 1 - Dockerize it

- **Milestone Participation due 3/30**

### Tasks

- Create new GitHub repo (link to create located in Pilot in Content -> Project 5)
  - Done 
- In a folder named `website`, add the contents of your website
  - created a basic html file located in the website folder. 
- Install Docker
  - To install Docker, I went back to the lecture and followed along as well as referred to this webiste below. 
https://docs.docker.com/engine/install/ubuntu/

  ![dockerinstall](https://user-images.githubusercontent.com/77417309/164245525-07896cdf-a235-4131-b2e8-22847c79f961.png)

- Create a container image that will run a webserver and contains your "website"
  - Using apache2 
 Commands Used: sudo docker build -t my-apache2 . , sudo docker run -dit --name my-running-app -p 8080:80 my-apache 2
 Resources: 
 https://hub.docker.com/_/httpd
- Create a Dockerfile with instructions on how to build the image
  - Docker file has been created with instructions on how to build image. 
- Add site content & Dockerfile to repo
  - localhost:8080

## Part 2 - GitHub Actions and DockerHub

- **Milestone Participation due 4/8**

### Tasks

- Create DockerHub account: https://hub.docker.com/ (select Free tier if prompted)
- Create Public Repository in DockerHub

![Screenshot from 2022-04-20 10-31-07](https://user-images.githubusercontent.com/77417309/164342779-2f772f48-b42f-4bf9-8152-37bcdc61fa6b.png)

- Set GitHub Secrets named DOCKER_USERNAME and DOCKER_PASSWORD with your respective information filled out.
  - 
- Set up GitHub Actions workflow to build and push docker image to DockerHub
  - Use workflow templated here: https://docs.github.com/en/actions/guides/publishing-docker-images#publishing-images-to-docker-hub

### Documentation

- Update `README.md` in main folder of your repo to include:

- Create DockerHub public repo
  - process to create
- Allow DockerHub authentication via CLI using Dockhub credentials
- Configure GitHub Secrets
  - what credentials are needed - DockerHub credentials (do not state your credentials)
  - set secrets and secret names
- Configure GitHub Workflow
  - variables to change (repository, etc.)

### Resources

- [GitHub Actions - Docker Docs](https://docs.docker.com/ci-cd/github-actions/)

## Part 3 - Deployment

- **Milestone Participation due 4/20**

### Tasks

- For this piece, use an EC2 instance.
- Install docker on the instance
- Create a webhook set up to automatically deploy updates to the container image

### Documentation

- Update `README.md` in main folder of your repo to include:
- Creating a webhook

### Resources

- [using github actions and webhooks](https://levelup.gitconnected.com/automated-deployment-using-docker-github-actions-and-webhooks-54018fc12e32)
- [Link needed - webhooks with DockerHub]

## Submission

1. Commit and push your changes to your repository. Verify that these changes show in your course  
   repository.

   - Your repo should contain:
   - `README.md`
   - `website` folder with website pages
   - `Dockerfile`
   - GitHub action yml file

2. In Pilot, paste the link to your project folder.

## Extra Credit - DIY

Worth 10%

Pick a project of yours or that you are interested in, and create a docker container of your project.

- Database
- Java program
- php site
- something else?

Document and include:

- Dockerfile that builds your project and environment
- Image with your project (link from DockerHub) / `docker pull` command
- Instructions to run container from image
