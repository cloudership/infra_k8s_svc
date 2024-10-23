# mlflow

## Set up

### Tracking Server

The tracking server uses the RDBMS configured in 10-secret.crypt.yaml

Check the top-level README for how to manage k8s secrets.

### Model Registry and Files

The model registry is configured to store artifacts in a bucket configured by the `ARTIFACTS_BUCKET` environment
variable, so add it to the `mlflow` Configmap/secret or configure it through IaC.

A service account must be given to the service that has a connected IAM role that has permission to write to that
bucket.

### Testing

[Test it and create test data by running this Python script that trains and logs a model](https://gist.github.com/ayqazi/beb5cea5dafc768a4522797105c9f72f)
