# terraform-modules-aws-sns-email-notification

Terraform does not support email notification  for sns subscriptions as this
would break the terraform concept. See here:

https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/sns_topic_subscription

This module is made for Terraform 12

## Example Usage

```
module "sns_email" {
  source = "github.com/noqqe/terraform-modules-aws-sns-email-notification?ref=v0.1.0"

  application_name      = "my-cloudwatch-alert"
  notification_endpoint = "team-alert@example.com"
}
```
