# gke-k8s-terraform-sample

These Terraform templates will provision a GKE cluster in GCP and deploy a nginx Pod.

## Getting project credentials
In order to deploy your workload to Google Cloud, you need to set up a service account key, which Terraform will use to create and manage resources in your GCP project. Go to the [create service account key page](https://console.cloud.google.com/apis/credentials/serviceaccountkey). Select the default service account or create a new one, select JSON as the key type, and click Create.

This downloads a JSON file with all the credentials that will be needed for Terraform to manage the resources. This file should be located in a secure place for production projects, but for this example move the downloaded JSON file to the project directory and replace the [credentials_sample.json](./credentials_sample.json)

## Getting started

```shell
$ terraform init
```

```shell
$ terraform plan
```

```shell
$ terraform apply
```