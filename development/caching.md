# Caching

## Why

Occasionally we need to cache data, either for a limited amount of time, or for the duration of a user's session.

## What

Our OpenShift cluster is peered with our "Data VPC", AKA "Virtual Private Cloud". We have Terraform playbooks that manage the use of [Amazon Elasticache](http://docs.aws.amazon.com/AmazonElastiCache/latest/UserGuide/WhatIs.html) to create performant, in-memory distributed caching environments, using the [Redis protocol](https://redis.io/commands).

## How

If you need a new Elasticache instance, accessible to either sandbox or main clusters, submit a pull request to our Data VPC Terraform repositories, respectively:

- [Data VPC MAIN](https://github.com/telusdigital/terraform-openshift-datavpc-main)
- [Data VPC SANDBOX](https://github.com/telusdigital/terraform-openshift-datavpc-sandbox)

To gain access to Amazon IAM, you can submit a pull request to the Data VPC IAM Terraform repository:

- [Data VPC IAM](https://github.com/telusdigital/terraform-openshift-datavpc-iam)

### Best practices

- Treat this like a cache, not a database. Assume all data is ephemeral and can be wiped at any moment.
- Encrypt any sensitive data using AES-256
- Set an expiry time to live (TTL), to ensure data is purged often

## Who

@delivery

## References

- [Elasticache Docs](http://docs.aws.amazon.com/AmazonElastiCache/latest/UserGuide/WhatIs.html)
- [Redis protocol](https://redis.io/commands)
- [Terraform Elasticache Module](https://github.com/telusdigital/terraform-aws_elasticache_cluster)
- [Data VPC MAIN](https://github.com/telusdigital/terraform-openshift-datavpc-main)
- [Data VPC SANDBOX](https://github.com/telusdigital/terraform-openshift-datavpc-sandbox)
- [Data VPC IAM](https://github.com/telusdigital/terraform-openshift-datavpc-iam)