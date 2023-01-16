# Multicontainer application
This application will make use of a seperate client, server and database. These will have their own docker files for image creation.
As well as a docker-compose file for combined container management.

Codeching - video 8 - Dockerizing a React application with Node.js Postgres and NginX - dev and prod - step by step - PART 1
It contains React client, Node.js backend, PostgreSQL and Nginx

## Resources
- (Gitlab)[https://gitlab.com/codeching/docker-multicontainer-application-react-nodejs-postgres-nginx-basic]
- (Video One)[https://www.youtube.com/watch?v=-pTel5FojAQ&ab_channel=Codeching]
- (Video Two)[]
- (Video Extra)[https://www.youtube.com/watch?v=3xDAU5cvi5E&ab_channel=SanjeevThiyagarajan]

## Getting started
Ensure your system has docker desktop running.

## Steps
1. Complete client/README.md AS Development
2. Complete server/README.md AS Development
3. Create docker-compose.yaml
4. Create /nginx/default.conf
5. Create /nginx/Dockerfile.dev
6. `docker-compose up --build` and navigate to `localhost:3050`
7. Complete client/README.md AS Production
8. Complete server/README.md AS Production

## Developer notes
Ensure docker desktop settings has kubernetees enabled

docker-compose will allow nginx, client and server together in local development environment. 

You can run it in development mode: docker-compose up --build
It contains Dockerfiles for client, server which you should push to your docker hub to be able to pull them down when in next tutorial we will use them in Kubernetes.

Upstream modules define group of servers that can be referenced by the proxy pass.
client is defined in docker-compose

## Commands

Build a docker image
> docker build -f Dockerfile.dev -t multi-server .

Run docker image
> docker run -it -p 4003:30002 multi-server

Save a docker image locally
> docker save -o <PATH> <IMAGE>

Push a docker image
> docker push multi-server

Load a docker image
> docker load -i <PATH>



