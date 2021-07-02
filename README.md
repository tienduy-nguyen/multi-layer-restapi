# Dockerize Nodejs React App on AWS

## Introduction

- [Part 1](https://itnext.io/dockerize-a-react-nodejs-app-and-deploy-in-aws-ec2-the-startup-way-part-1-b398d71c384b)
- [Part 2](https://itnext.io/dockerize-a-react-nodejs-app-and-deploy-in-aws-ec2-the-startup-way-part-2-303921149faf)

## Docker images

Push docker images

```dockerfile
docker push <your username>/<reponame>:production_14062021_postgres
docker push <your username>/<reponame>:production_14062021_api
docker push <your username>/<reponame>:production_14062021_ui

example:
docker push kanlanc/vikranth:production_14062021_ui

(or)

docker push <your username>/<reponame> --all-tags
```