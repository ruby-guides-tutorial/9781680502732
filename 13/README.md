# 13 A Production-Like Playground

|本期版本|上期版本
|:---:|:---:
`Tue Aug  8 15:43:54 CST 2023` | -


## Creating Machines(废弃)

**macOS**

> `13.5`

```
brew install docker-machine
```


```
docker-machine create --driver virtualbox local-vm-1
docker-machine ssh local-vm-1
```

## Configuring the Docker CLI

```
docker-machine env local-vm-1
```


## Introducing Docker Swarm


> `@pending`

## Ref

* <https://github.com/docker/machine>
* <https://github.com/boot2docker/boot2docker>