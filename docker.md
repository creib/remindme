# Docker commands...

## cleanup
```
docker system df
docker system prune

# delete all local images
docker rmi -f $(docker images -aq)

```
