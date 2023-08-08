# 07 Playing Nice with JavaScript

|本期版本|上期版本
|:---:|:---:
`Tue Aug  8 14:00:35 CST 2023` | 


## The JavaScript Front-End Options


* Sprockets


## Rails JavaScript Front End with Webpacker

```bash
rails new myapp --webpack=react
```

```bash
# gem 'webpacker', '~> 3.5'
bin/rails webpacker:install

bin/rails webpacker:install:react
```


## Compiling Assets with Webpacker

```yml
command: ./bin/webpack-dev-server
ports:
  - 3035:3035
environment:
  - WEBPACKER_DEV_SERVER_HOST=0.0.0.0
```