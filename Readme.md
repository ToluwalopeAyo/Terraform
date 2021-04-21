## Provisioning A Kubernetes Cluster and A GCE instance Using Terraform

In the main.tf file there's the provider block that shows I used the Google provider for GCP.

I used several modules for the provisioning.

I used the **gke_auth** module to configure authentication and authorisation for the cluster, **gcp_network** module to create a VPC dedicated to the cluster, **gke** module to provision the cluster itself.

The **google_compute_instance** resource is to provision the gce vm.

The varible.tf fle is to define parameters for the cluster and the output.tf file is to define output

Run ```terraform init``` to initialize terraform

```terraform plan```

The output is a detailed summary of resources that will be creater

```terraform apply```

This would create the resources in the specified project-id
