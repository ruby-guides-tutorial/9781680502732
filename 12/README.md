# 12 Preparing for Production

|本期版本|上期版本
|:---:|:---:
`Tue Aug  8 15:21:52 CST 2023` | -


## Configuring a Production Environment

> `.env/production`

```
RAILS_ENV=production				# app starts in production mode
SECRET_KEY_BASE=						# sign the cookies
RAILS_LOG_TO_STDOUT=true			# logs/<environment>.log
RAILS_SERVE_STATIC_FILES=true
```

```bash
bin/rails secret
```


## A Production Image: Precompiling Assets


> `Dockerfile.prod`

```
RUN bin/rails assets:precompile
```

## Sharing Images


* Docker Registries、Docker Hub

```
[<registry hostname>[:port]/]<username>/<image name>[:<tag>]
```


## Pushing Our Image to a Registry

```
docker tag <image ref> robisenberg/<image_name>
docker build -f Dockerfile.prod -t robisenberg/myapp_web:prod .
```
```
docker login
docker push robisenberg/myapp_web:prod
```


## Ref

* <https://hub.docker.com/_/registry>