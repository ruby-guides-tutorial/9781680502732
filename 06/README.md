# 06 Adding a Database: Postgres

|本期版本|上期版本
|:---:|:---:
`Sat Jul 22 14:15:26 CST 2023` | `Fri Aug 26 13:08:09 CST 2022`


## Creating Our App Databases

```yaml
environment:
	POSTGRES_USER: postgres
	POSTGRES_PASSWORD: exmaple
```


```yaml
env_file:
	- .env/development/web
```


## Decoupling Data from the Container

```yaml
services:
	database:
		image: postgres
		volumes:
		- db_data:/var/lib/postgresql/data
volumes:
	db_data:
```

```bash
docker volume inspect myapp_mysql_data
```