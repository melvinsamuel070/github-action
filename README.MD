# INSTALLATION OF DOCKER
this githube install using official docker installation command


## USAGE
To use this action yuor repository, create a workflow (e.g,   ` .github/workflows/install-docker.yaml`) and the following  content:

```yaml
name: install-container-action
on: [push]
jobs:
  install-container-action:
      runs-on: ubuntu-latest
      steps:
       -name: checkout repository
       -uses: action/checkout@v3
       -name: install Docker
       -uses: melvinsamuel070/install-docker-actions@v1
       -name: Run Docker Image 
        run: docker build -t the-image:1
       -name: version
        run: docker --version
       -name: Run test
        run: docker run the-image:1 test
