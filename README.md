PoC of using flux + helm to deploy to a GKE cluster and run tests

Bootstrapping:

Install glcoud - brew install --cask google-cloud-sdk / choco install gcloudsdk

Initialize gcloud - gcloud init; gcloud auth application-default login

Terraform:

Initialize workspace - terraform init (in root dir)

Apply - terraform apply (--auto-approve (optional))

Kubectl:

Get creds - gcloud container clusters get-credentials $(terraform output -raw kubernetes_cluster_name) --region $(terraform output -raw region)

Verify - kubectl cluster-info
