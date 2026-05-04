# Docker Practical – SET B

## Build Image
docker build -t myapp .


## Run Private Registry
docker run -d -p 5001:5000 --name registry registry:2


## Tag Image
docker tag myapp localhost:5001/myapp


## Push Image
docker push localhost:5001/myapp


## Verify Registry
curl http://localhost:5001/v2/_catalog


Output:
{"repositories":["myapp"]}


## Run Container
docker run -d -p 3000:3000 myapp


## Test Application
curl http://localhost:3000

Output:
Hello Docker 🚀


## Rebuilt using

docker build --no-cache -t myapp .

