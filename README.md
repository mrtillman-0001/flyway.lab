# flyway

---

Docker Container: https://hub.docker.com/r/flyway/flyway/

```sh
$ docker run --rm \
-v /home/stephen/Lab/flyway/sql:/flyway/sql \
-v /home/stephen/Lab/flyway/conf:/flyway/conf \
flyway/flyway info
```