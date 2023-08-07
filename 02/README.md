# 02 Running a Rails App in a Container

|本期版本|上期版本
|:---:|:---:
`Mon Aug  7 20:12:48 CST 2023` | `Fri Jul 21 20:20:10 CST 2023`


## Defining Our First Custom Image

```bash
apt-get update -yqq
apt-get install -yqq --no-install-recommends nodejs
```

## Running a Rails Server with Our Image

```bash

docker run -p 3000:3000 a1df0eddba18 \
	bin/rails s -b 0.0.0.0
```

**Finding the IP Address of a Running Container**

```bash
docker inspect --format \
'{{ .NetworkSettings.IPAddress }}' d7230c4b0595
```
