# 05 Beyond the App: Adding Redis

|本期版本|上期版本
|:---:|:---:
`Mon Aug  7 21:09:48 CST 2023` | `Fri Jul 21 20:50:14 CST 2023`

## How Containers Can Talk to Each Other

```bash
docker network ls
```

* Compose uses the service name (as defined in our docker-compose.yml) as the DNS entry