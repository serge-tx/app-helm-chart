# webapp-helm-chart
Contains the generic helm chart for a web application. It is used by Prometheus & Disco project

## Usage

Reference the release of the chart you want to deploy in terraform

```hcl
resource "helm_release" "app" {
  chart     = "https://github.com/DND-IT/webapp-helm-chart/archive/0.0.2.tar.gz"
  ...
}
```

## AWS Role

If you specify a IAM role in `aws_iam_role_arn` a service account will be create to take advantage of [fine grained permission for pods](https://aws.amazon.com/blogs/opensource/introducing-fine-grained-iam-roles-service-accounts/)