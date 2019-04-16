# CF Templates

## Static Website

```json
{
    "Resources": {
        "Stack": {
            "Type": "AWS::CloudFormation::Stack",
            "Properties": {
                "TemplateUrl": "https://s3.amazonaws/cf-templates/static/template.json",
                "Parameters": {
                    "DomainName": "<full_domain_name>",
                    "HostedZoneId": "<hosted_zone_id>",
                    "AcmCertificateArn": "<certificate_arn>"
                }
            }
        }
    }
}
```

## ECS Cluster

```json
{
    "Resources": {
        "Stack": {
            "Type": "AWS::CloudFormation::Stack",
            "Properties": {
                "TemplateUrl": "https://s3.amazonaws/cf-templates/ecs-cluster/template.json",
                "Parameters": {
                    "ClusterName": "<cluster_name>"
                }
            }
        }
    }
}
```