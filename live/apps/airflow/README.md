# airflow

## Install/upgrade

Pull latest airflow with:

```shell
helm pull airflow --repo https://airflow.apache.org
```

At time of writing it pulls 1.15.0. Install it with:

```shell
(cd live/apps/airflow && helm upgrade --install airflow ./airflow-1.15.0.tgz --namespace airflow --create-namespace --values values.yaml --values values.crypt.yaml)
```

Then apply the manifests:
```shell
kubectl apply -f live/apps/airflow/60-targetgroupbinding.yaml
kubectl apply -f live/apps/airflow/10-gitsync-secret.crypt.yaml
```
