## Running a MySQL container
- Check the documentation for the required variables. For MySQL containers you must set `MYSQL_ROOT_PASSWORD`
- Applications also set their own environment variables
- For security and portability you want to set those environment variables either at runtime, or in a separate configuration file that doesn't get version controlled in a public repo.

**Example command to run a MySQL container**

```
$ docker run --name mysql -p 3306:3306 \                        
-e MYSQL_ROOT_PASSWORD=some-password \
-e MYSQL_DATABASE=some-database \
-e MYSQL_USER=some-admin \
-e MYSQL_PASSWORD=some-user-password \
-d mysql:latest
```