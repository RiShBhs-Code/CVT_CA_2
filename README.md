# First Docker Image (Very Simple)

This is a tiny Python web server project you can use for your first Docker Hub push.

## 1) Build the image

Replace `your_dockerhub_username` with your Docker Hub username.

```bash
docker build -t your_dockerhub_username/first-image:1.0 .
```

## 2) Run locally

```bash
docker run --rm -p 8000:8000 your_dockerhub_username/first-image:1.0
```

Open: http://localhost:8000

You should see:

```text
Hello! This is my first Docker image.
```

## 3) Login to Docker Hub

```bash
docker login
```

## 4) Push image to Docker Hub

```bash
docker push your_dockerhub_username/first-image:1.0
```

## 5) Optional: Add `latest` tag and push

```bash
docker tag your_dockerhub_username/first-image:1.0 your_dockerhub_username/first-image:latest
docker push your_dockerhub_username/first-image:latest
```
