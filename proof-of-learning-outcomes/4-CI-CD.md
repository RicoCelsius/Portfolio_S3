# Learning outcome 4: Implement a (Semi-)Automated Software Release Process
## In short:
You implement a (semi-)automated software release process that matches the needs of the project context.

### Implementation:
In the modern software development lifecycle, automating the release process is crucial for efficiency and reliability. It involves setting up systems that handle the integration and deployment of new code changes automatically. Key aspects include:

- **Continuous Integration and Deployment (CI/CD)**: You set up a CI/CD pipeline using tools like GitLab CI and Docker. This involves automating the integration of code changes from multiple contributors and ensuring that the software is reliably released to production without manual intervention.
- **Docker**: You use Docker to create containers that package your software with all its dependencies, making it easy to deploy consistently across any environment.

# Proof
To demonstrate continuous integration and continuous deployment (CI/CD). We have created a number of pipelines using Github actions. These pipelines ensure that our code is automatically tested, automatically goes to the static code analyzer and is vetted and also that unit tests start running. When all unit tests pass, then a push is automatically made to Dockerhub. Then, using Watchtower, the server sees that a new image is available. This image is pulled and the old container is stopped. A new container with the new image is then created and run.
## CI/CD Pipeline Implementation
- [Link to the CI/CD pipeline setup or configuration files](https://github.com/NuanceDevs/Api-Gateway/actions/runs/7115536557/workflow)
- [Screenshots or documentation showing the pipeline in action](https://i.postimg.cc/VvXvqDsn/image.png)

## Docker Implementation
- [Dockerfile and related configuration files](https://github.com/NuanceDevs/Api-Gateway/blob/main/Dockerfile)

