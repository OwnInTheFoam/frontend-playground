# Multiapp client
To create react application from scratch
```
npx create-react-app
```

## Installation
```
npm install
```

## Running
```
npm run start
```

Then navigate to `localhost:30001` to confirm react application available.

Note client will call "/api/values" while node server will only define "/values"
  Nginx will redirect "/api/values" to node server as "/values"

## Development

Create Dockerfile.dev
```
docker build -f Dockerfile.dev -t drdre08/multi-client .
docker run -it -p 4002:30001 drdre08/multi-client
```
Ensure application client is running at `localhost:4002`

## Production

Create Dockerfile
```
docker build -t drdre08/multi-client .
docker run -it -p 30001:30001 drdre08/multi-client
```
Check `localhost:30001`

You need to push your build imagine to docker hub to pull images for kubernetes.
```
docker push drdre08/multi-client
```