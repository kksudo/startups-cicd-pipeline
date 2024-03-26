# Docker Compose CI/CD Pipeline

This repository provides a streamlined CI/CD pipeline for deploying Docker Compose applications on VPS-style instances (e.g., AWS EC2, DigitalOcean Droplets) using GitHub Actions. It simplifies your development workflow and ensures seamless deployments with our ready-to-use GitHub Action configurations and Docker setup.

**N.B.** Feel free to open a [new issue](https://github.com/kksudo/startups-cicd-pipeline/issues) if you need this pipeline to support additional features or have any questions.

## Features

- **Automated Testing**: Run tests automatically to ensure code integrity before deployment.
- **Docker Image Build**: Automatically build your Docker image as part of the CI pipeline.
- **Seamless Deployments**: Deploy your Docker Compose application to a VPS with minimal setup, supporting platforms like EC2, DigitalOcean, Hetzner, etc...
- **Pre-configured GitHub Actions**: Utilize our GitHub Actions workflow for a hands-off approach to CI/CD.

## Prerequisites

Before you begin, ensure you have the following:
- A [GitHub account](https://github.com/join)
- A VPS (e.g., AWS EC2, DigitalOcean Droplet) with Docker and Docker Compose installed
  - [AWS Free Tier for 1 year](https://aws.amazon.com/free)
  - [DigitalOcean Free $200 Credit](https://try.digitalocean.com/freetrialoffer/)
- [SSH access to your VPS](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/connect-linux-inst-ssh.html)

## Quick Start

1. **Fork or Clone This Repository**

   Start by forking or cloning this repository to your GitHub account.

2. **Configure GitHub Secrets**

   Navigate to your repository settings, find the Secrets section, and add the following:
    - `HOST`: Your VPS IP address or domain name.
    - `SSH_KEY`: Your private SSH key (base64 encoded) for server access.
    - `USER`: The SSH user for your server.

3. **Customize Your Docker Compose Setup**

   Modify the `compose.yml` file in the repository to suit your application's needs.

4. **Push Changes**

   Any push to your `main`(default) branch will trigger the CI/CD pipeline, running tests, building your Docker image, and deploying your application to your VPS.

## Workflow Details

The GitHub Actions workflow consists of the following steps:

1. **Checkout**: Checks out your repository for GitHub Actions.
2. **Set Up Docker Buildx**: Prepares the Docker build environment.
3. **Run Tests**: Executes your application tests.
4. **Build and Push Docker Image**: Builds your Docker image and pushes it to a registry if specified.
5. **Deploy to VPS**: Connects to your VPS via SSH and deploys your Docker Compose application.

## Contributing

[Contributions](/.github/CONTRIBUTING.md) are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

Distributed under the MIT License.

## Contact

Twitter - [@kk_sudo](https://twitter.com/kk_sudo)

LinkedIn - [Kirill](https://www.linkedin.com/in/kazakovk/)

Project Link: [https://github.com/kksudo/startups-cicd-pipeline](https://github.com/kksudo/startups-cicd-pipeline)
