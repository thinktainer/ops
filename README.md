# ops faq

This is my personal ops faq. I dump stuff i find useful in here, so I don't have to remember.

## benthos

### Q: how do i run benthos in docker, connecting to an existing docker-compose network (kafka)
Get `<compose-network>` with docker network ls.

```
docker run -ti \
	-v$PWD/3-s3-kafka.yaml:/benthos.yaml \
	-v$PWD/logger.yaml:/logger.yaml \
	--network <compose-network> \
	<registry>/benthos
```

## kubernetes

### Q: how do i set autodeploy to off?

```
kubectl label --overwrite namespace `my-namespace` automaticDeployment=off
```

