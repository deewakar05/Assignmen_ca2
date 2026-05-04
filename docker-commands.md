# Docker Practical – SET B

## Build Image

```bash
docker build -t myapp .
```

## Run Private Registry

```bash
docker run -d -p 5001:5000 --name registry registry:2
```

## Tag Image

```bash
docker tag myapp localhost:5001/myapp
```

## Push Image

```bash
docker push localhost:5001/myapp
```

## Verify Registry

```bash
curl http://localhost:5001/v2/_catalog
```

Output:

```json
{"repositories":["myapp"]}
```

## Run Container

```bash
docker run -d -p 3000:3000 myapp
```

## Test Application

```bash
curl http://localhost:3000
```

Output:

```
Hello Docker 🚀
```

# **Rebuilt using**

docker build --no-cache -t myapp .
