# airflow

## Install/upgrade

Pull latest airflow with:

```shell
helm pull airflow --repo https://airflow.apache.org
```

At time of writing it pulls 1.15.0. Install it with:

```shell
helm upgrade --install airflow ./airflow-1.15.0.tgz --namespace airflow --create-namespace --values values.crypt.yaml
```
