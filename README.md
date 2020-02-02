# gke-k8s-terraform-sample

These Terraform templates will provision a GKE cluster in GCP and deploy a nginx Pod.

## Prerequisites

- Google Cloud Account
- [Terraform](https://www.terraform.io/downloads.html)


## Getting project credentials
In order to deploy your workload to Google Cloud, you need to set up a service account key, which Terraform will use to create and manage resources in your GCP project. Go to the [create service account key page](https://console.cloud.google.com/apis/credentials/serviceaccountkey). Select the default service account or create a new one, select JSON as the key type, and click Create.

This downloads a JSON file with all the credentials that will be needed for Terraform to manage the resources. This file should be located in a secure place for production projects, but for this example move the downloaded JSON file to the project directory and replace the [credentials.json](./credentials.json)

## Getting started

```shell
$ terraform init

Initializing the backend...

Initializing provider plugins...
- Checking for available provider plugins...
- Downloading plugin for provider "google" (hashicorp/google) 3.6.0...
- Downloading plugin for provider "kubernetes" (hashicorp/kubernetes) 1.10.0...

The following providers do not have any version constraints in configuration,
so the latest version was installed.

To prevent automatic upgrades to new major versions that may contain breaking
changes, it is recommended to add version = "..." constraints to the
corresponding provider blocks in configuration, with the constraint strings
suggested below.

* provider.google: version = "~> 3.6"
* provider.kubernetes: version = "~> 1.10"

Terraform has been successfully initialized!

You may now begin working with Terraform. Try running "terraform plan" to see
any changes that are required for your infrastructure. All Terraform commands
should now work.

If you ever set or change modules or backend configuration for Terraform,
rerun this command to reinitialize your working directory. If you forget, other
commands will detect it and remind you to do so if necessary.
```

```shell
$ terraform plan
```

```shell
$ terraform apply
```
