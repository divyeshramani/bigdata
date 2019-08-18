# Setup Zepllin in Docker

Start Zeplin docker container with mounnted volume for logs and notebooks to persist.
```
docker run -d -p 8081:8080 --rm -v $PWD/logs:/logs -v $PWD/notebook:/notebook -e ZEPPELIN_LOG_DIR='/logs' -e ZEPPELIN_NOTEBOOK_DIR='/notebook' --name zeppelin apache/zeppelin:0.8.0
```
Hit url http://<docker_host>:8081/