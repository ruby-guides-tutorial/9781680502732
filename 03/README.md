# 03 Fine-Tuning Our Rails Image

|本期版本|上期版本
|:---:|:---:
`Mon Aug  7 20:20:24 CST 2023` | `Fri Jul 21 20:30:25 CST 2023`

## Naming and Versioning Our Image

```
docker tag a1df0eddba18 railsapp
```

## A Default Command

```
CMD ["bin/rails", "s", "-b", "0.0.0.0"]
```


## Ignoring Unnecessary Files

> `.dockerignore`

```bash
#Git
.git
.gitignore

# Logs
log/*

# Temp files
tmp/*

# Editor temp files
*.swp
*.swo
```

## The Image Build Cache

```bash
apt-get update -yqq && apt-get install -yqq --no-install-recommends \
	nodejs
```

## The Gemfile Caching Trick

```bash
COPY Gemfile* /usr/src/app/
WORKDIR /usr/src/app
RUN bundle install

COPY . /usr/src/app
```

## The Finishing Touch


```
LABEL <key>=<value>
```