# 10 Some Minor Irritations

|本期版本|上期版本
|:---:|:---:
`Tue Aug  8 14:45:40 CST 2023` | -


## Rails tmp/pids/server.pid Not Cleaned Up

```bash
rm tmp/pids/server.pid
docker-compose up
```


* `exec`: Replace the currently running process (this Bash script) by running the following
* `$@`: all arguments that were provided to this Bash script

## Compose Intermittently Aborts with Ctrl-C


* sending the main process the `SIGTERM` signal