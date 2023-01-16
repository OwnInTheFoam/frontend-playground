# Multiapp server

## Installation
```
npm run install
```

## Running
```
npm run dev
```
Navigate to `localhost::30002` to ensure server is accessable.

## Development

Create Dockerfile.dev
```
docker build -f Dockerfile.dev -t drdre08/multi-server .
docker run -it -p 4003:30002 drdre08/multi-server
```
Ensure application server is running at `localhost:4003`

## Production

Create Dockerfile
```
docker build -t drdre08/multi-server .
docker run -it -p 30002:30002 drdre08/multi-server
```
Navigate to `localhost:30002`.

You need to push your build imagine to docker hub to pull images for kubernetes.
```
docker push drdre08/multi-server
```