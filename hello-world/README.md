### Create image
```
docker build -t hello:1.0 .
docker image ls
```

### Push image to Docker Hub
```
export USER=p0gram3r

docker tag hello:1.0 $USER/hello:1.0
docker login -u $USER
docker push $USER/hello:1.0
docker logout
```

### Push image to private repository
```
export USER=(user-id)
export REPO=(repo-url)

docker tag hello:1.0 $REPO/hello:1.0
docker login -u $USER $REPO
docker push $REPO/hello:1.0
docker logout $REPO
```