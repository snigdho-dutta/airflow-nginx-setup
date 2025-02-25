# Airflow With Nginx Configuration In Docker

## ```Folder Structure```

- airflow/
  - dags/
  - config
  - logs/ (gitignored)
  - plugins/
  - Dockerfile
  - requirements.txt
- nginx/
  - conf.dev.d/
    - airflow.conf
  - conf.prod.d/
    - airflow.conf
  - Dockerfile
- compose.yml

```.env``` Variables

- NGINX_CONF_DIR
- FERNET_KEY
- AIRFLOW_PROJ_DIR
- AIRFLOW_UID
- _AIRFLOW_WWW_USER_USERNAME
- _AIRFLOW_WWW_USER_PASSWORD
... (see [documentation](https://airflow.apache.org/docs/docker-stack/quickstart.html#environment-variables))

### Additional Tweaks

Here we are using `LocalExecutor`, and we have disabled default `Celery` (CeleryWorker Executor), `Redis` (Message Queue) and `Flower` (Celery UI)  in compose.yml.
