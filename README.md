HA Vault Cluster
================

This repository has two components

- Packer script to create GCP VM Image to be used in the cluster.
- Terraform scripts to deploy HA Vault Cluster.

The Vault cluster stores data in GCS bucket and gets auto-unsealed by using Google KMS.

Create Packer Image
===================

```
packer build packer/vault.json
```

Run Terraform 
=============

```
terraform init
terraform plan
terraform apply --auto-approve
```
