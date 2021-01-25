# flyway

version control for your database

---

## Resources

- [Flyway Quickstart](https://flywaydb.org/documentation/getstarted/firststeps/commandline)
- [Flyway University](https://www.red-gate.com/hub/university/courses/flyway/getting-started-with-flyway)

## Usage 

1. Pull the [Flyway Docker Container](https://hub.docker.com/r/flyway/flyway/)
2. Rename flyway demo config from `./flyway.conf.demo` to `./flyway.conf`.
3. Edit `./flyway.conf`
    - flyway.url=`jdbc:{connection_string}`
    - flyway.user=`{db_username}`
    - flyway.password=`{db_password}`
4. Add migration scripts to `./sql` folder.
    - V1__Create_person_table.sql
    - V2__Add_people.sql

```sh
# run flyway commands
$ docker run --rm \
  -v /home/mrtillman/Lab/flyway/sql:/flyway/sql \
  -v /home/mrtillman/Lab/flyway/conf:/flyway/conf \
  flyway/flyway info
```
