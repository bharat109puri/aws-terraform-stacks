# AWS Elastic Container Service (ECS) Terraform module

Terraform module which creates ECS resources on AWS.

This module focuses purely on ECS and nothing else. Therefore only these resources can be created with this module:

* [ECS](https://www.terraform.io/docs/providers/aws/r/ecs_cluster.html)
* [IAM](https://www.terraform.io/docs/providers/aws/r/iam_instance_profile.html)

However, having said the above to have a proper ECS cluster up and running multiple resources are needed. In most cases creating these resources is heavily opinionated and or context-bound. That is why this module does not create these resources. But you still need them to have a production ready environment. Therefore the example area shows how to create everything needed for a production environment.

## Usage

```hcl
module "ecs" {
  source = "terraform-aws-modules/ecs/aws"

  name = "example-ecs"
}
```


## Authors
* **Bharat Puri**  -  *bhpuri@gmail.com*  

## License

This project is licensed under the MIT License - see the [LICENSE.md](../LICENSE.md) file for details
