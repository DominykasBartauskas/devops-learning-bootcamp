
# DevOps Learning Bootcamp (5-Day Plan)

## Overview
This repository contains a structured 5-day learning plan designed to help you understand and apply essential DevOps tools and practices including GitLab CI/CD pipelines, Docker, and modern software development workflows.

---

## 📅 Day 1: Foundations & Setup

**Goal**: Understand the development workflow and set up your environment.

### Topics
- Overview of modern development workflows (CI/CD, containers, merge requests)
- Git and GitLab basics

### Activities
- Install Git, Docker, and a code editor (e.g., VS Code or PyCharm)
- Create a GitLab account and clone a sample repository
- Read:
  - [GitLab Flow](https://docs.gitlab.com/ee/topics/gitlab_flow.html)
  - [Git basics](https://www.atlassian.com/git/tutorials/what-is-version-control)

### Hands-on
- Create a new repo with a `README.md`
- Make a branch, change the README, push it, and open a Merge Request (MR)

---

## 📅 Day 2: Docker Basics

**Goal**: Learn containerization and Dockerfile creation.

### Topics
- What is Docker? Why use containers?
- Dockerfile, images vs containers, volumes, networks

### Activities
- Read:
  - [Docker Getting Started](https://docs.docker.com/get-started/)
  - [Dockerfile Reference](https://docs.docker.com/engine/reference/builder/)

### Hands-on
- Create a `Dockerfile` for a simple Python or Node.js app
- Build and run the Docker container locally
- (Optional) Push the image to Docker Hub

---

## 📅 Day 3: GitLab CI/CD Pipelines

**Goal**: Understand and configure basic GitLab Pipelines.

### Topics
- What is CI/CD? Pipeline stages and jobs
- `.gitlab-ci.yml` syntax

### Activities
- Read:
  - [GitLab CI/CD Pipelines](https://docs.gitlab.com/ee/ci/)
  - [YAML basics](https://learnxinyminutes.com/docs/yaml/)

### Hands-on
- Add a `.gitlab-ci.yml` file:
  ```yaml
  stages:
    - test

  test_job:
    stage: test
    script:
      - echo "Running tests..."
      - echo "All tests passed!"
  ```
- Push and watch the pipeline run in GitLab

---

## 📅 Day 4: Connect Docker with GitLab CI/CD

**Goal**: Use Docker inside GitLab pipelines.

### Topics
- Using Docker in `.gitlab-ci.yml`
- GitLab runners and Docker-in-Docker (DinD)

### Activities
- Read:
  - [Use Docker in GitLab CI](https://docs.gitlab.com/ee/ci/docker/using_docker_build.html)

### Hands-on
- Add a pipeline step to build a Docker image:
  ```yaml
  build:
    stage: build
    image: docker:latest
    services:
      - docker:dind
    variables:
      DOCKER_TLS_CERTDIR: ""
    script:
      - docker build -t my-image-name .
  ```

---

## 📅 Day 5: Review & Practice

**Goal**: Reinforce what you've learned and apply feedback-based iteration.

### Activities
- Review pipeline, Dockerfile, and MRs
- Request code review and iterate based on feedback
- Troubleshoot and refine based on feedback

### Bonus
- Use AI tools to optimize `.gitlab-ci.yml` and Dockerfile
- Explore `.env` files and Docker volumes

---

## 📘 Repository Info

**Name**: `devops-learning-bootcamp`  
**Description**: A 5-day hands-on journey to master essential DevOps tools and workflows including GitLab CI/CD pipelines, Docker, and modern collaborative development practices.
