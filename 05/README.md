# 05 Beyond the App: Adding Redis

|本期版本|上期版本
|:---:|:---:
`Fri Jul 21 20:50:14 CST 2023` | `Tue Aug  9 14:54:39 CST 2022`

## How Containers Can Talk to Each Other

```bash
docker network ls
```

* Compose uses the service name (as defined in our docker-compose.yml) as the DNS entry