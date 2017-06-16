# Databases

## Why

Occasionally we need to cache data, either for a limited amount of time, or for the duration of a user's session.

## What

Our OpenShift cluster is peered with our "Data VPC", AKA "Virtual Private Cloud". We have Terraform playbooks that manage the use of [Amazon RDS](http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Welcome.html) to create managed relational databases in the cloud.

## How

If you need a new RDS instance, accessible to either sandbox or main clusters, submit a pull request to our Data VPC Terraform repositories, respectively:

- [Data VPC MAIN](https://github.com/telusdigital/terraform-openshift-datavpc-main)
- [Data VPC SANDBOX](https://github.com/telusdigital/terraform-openshift-datavpc-sandbox)

To gain access to Amazon IAM, you can submit a pull request to the Data VPC IAM Terraform repository:

- [Data VPC IAM](https://github.com/telusdigital/terraform-openshift-datavpc-iam)

### Best practices

TODO `¯\_(ツ)_/¯`

## Who

@delivery

## References

- [RDS Docs](http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Welcome.html)
- [Terraform RDS module](https://github.com/telusdigital/terraform-aws_rds_cluster)
- [Data VPC MAIN](https://github.com/telusdigital/terraform-openshift-datavpc-main)
- [Data VPC SANDBOX](https://github.com/telusdigital/terraform-openshift-datavpc-sandbox)
- [Data VPC IAM](https://github.com/telusdigital/terraform-openshift-datavpc-iam)