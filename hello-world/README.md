Simple Docker image that prints "hello world" to the console. A custom name can be passed as argument.
Provides a second entrypoint to say farewell.

### Build image
```
docker build -t hello:1.0 .
docker image ls
```

### Run container
```
# prints "hello world"
docker run hello:1.0

# greet homer
docker run hello:1.0 homer

# say farewell to homer
docker run --entrypoint farewell hello:1.0 homer
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