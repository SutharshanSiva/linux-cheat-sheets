# AWS CLI commands

[Back](README.md) to Linux CheatSheets by Ireaneus

```bash
aws --version
aws ec2 iam help
```

#### AWS CLI EC2 commands

```bash
aws ec2 describe-security-groups --output table
aws ec2 describe-regions --output table
aws ec2 describe-availability-zones --output table
aws ec2 describe-instances --output table
aws ec2 describe-images --image-id ami-6df1e514 --output table
aws ec2 describe-key-pairs
aws ec2 describe-security-groups --group-id sg-51d1612b --output table
aws ec2 run-instances --image-id ami-6df1e514 --count 1 --instance-type t2.micro --key-name MyWebAWS --user-data file://my_userdata.sh --subnet-id subnet-eec66eb5 --security-group-ids sg-51d1612b
aws ec2 describe-instance-attribute --instance-id i-054acd6b61b1b3c91 --attribute userData --output text --query "UserData.Value" | base64 --decode
aws ec2 describe-instances --instance-id i-054acd6b61b1b3c91 --output table
aws ec2 describe-instances --query 'Reservations[].Instances[].[Placement.AvailabilityZone,InstanceId,InstanceType,State.Name,Tags[Key=='Name'] | [0].Value]' --output table
aws ec2 get-console-output --instance-id i-0cb92fcf5285829c1 | sed 's/\\n/\n/g' | sed 's/\\r/\r/g'
aws ec2 terminate-instances --instance-ids i-0cb92fcf5285829c1 --dry-run
```

#### AWS CLI IAM commands

```bash
aws iam list-users
aws iam list-groups
aws iam list-roles
aws iam create-user --user-name TaosUser
aws iam create-access-key --user-name TaosUser
aws iam create-group --group-name Developers
aws iam add-user-to-group --user-name TaosUser --group-name Developers
aws iam list-policies --scope AWS | more
aws iam attach-group-policy --policy-arn arn:aws:iam::aws:policy/AmazonEC2FullAccess --group-name Developers
aws iam list-attached-group-policies --group-name Developers
aws iam list-attached-group-policies --group-name SystemAdmin
aws iam create-service-linked-role --aws-service-name SERVICE-NAME-URL.amazonaws.com
```

#### AWS CLI S3 commands

aws s3 cp ls mb mv presign rb rm sync website

```bash
aws s3 ls s3://mybucket
aws s3 cp myfolder s3://mybucket/myfolder --recursive
aws s3 sync myfolder s3://mybucket/myfolder --exclude *.tmp
```

#### AWS CLI SSM commands

```bash
aws ssm list-documents --output table
aws ssm describe-instance-information --output text --query "InstanceInformationList[*]"
aws ssm send-command --document-name "AWS-RunShellScript" --comment "listing services" --instance-ids "i-0cb92fcf5285829c1" --parameters commands="service --status-all" --region us-west-2 --output text
aws ssm list-command-invocations --command-id "command ID" --details
aws ssm describe-document --name "AWS-RunShellScript" --query "[Document.Name,Document.Description]"
aws ssm describe-document --name "AWS-RunShellScript" --query "Document.Parameters[*]"
aws ssm describe-instance-information --instance-information-filter-list key=InstanceIds,valueSet=i-0cb92fcf5285829c1
aws ssm describe-instance-information --instance-information-filter-list key=AgentVersion,valueSet=LATEST
```

#### AWS CLI All Resources

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| acm | cognito-idp | elb | lightsail | servicecatalog |
| apigateway | cognito-sync | elbv2 | logs | ses |
| application-autoscaling | configservice | emr | machinelearning | shield |
| appstream | configure | es | marketplacecommerceanalytics | sms |
| athena | cur | events | marketplace-entitlement | snowball |
| autoscaling | datapipeline | firehose | meteringmarketplace | sns |
| batch | deploy | gamelift | mturk | sqs |
| budgets | devicefarm | glacier | opsworks | ssm |
| clouddirectory | directconnect | greengrass | opsworks-cm | stepfunctions |
| cloudformation | discovery | health | organizations | storagegateway |
| cloudfront | dms | iam | pinpoint | sts |
| cloudhsm | ds | importexport | polly | support |
| cloudsearch | dynamodb | inspector | rds | swf |
| cloudsearchdomain | dynamodbstreams | iot | redshift | waf |
| cloudtrail | ec2 | iot-data | rekognition | waf-regional |
| cloudwatch | ecr | kinesis | resourcegroupstaggingapi | workdocs |
| codebuild | ecs | kinesisanalytics | route53 | workspaces |
| codecommit | efs | kms | route53domains | xray |
| codepipeline | elasticache | lambda | s3 | codestar |
| elasticbeanstalk | lex-models | s3api | cognito-identity | elastictranscoder |
| lex-runtime | sdb |

#### AWS cloudformation

```bash
  create-stack
--stack-name <value>
[--template-body <value>]
[--template-url <value>]
[--parameters <value>]
[--disable-rollback | --no-disable-rollback]
[--rollback-configuration <value>]
[--timeout-in-minutes <value>]
[--notification-arns <value>]
[--capabilities <value>]
[--resource-types <value>]
[--role-arn <value>]
[--on-failure <value>]
[--stack-policy-body <value>]
[--stack-policy-url <value>]
[--tags <value>]
[--client-request-token <value>]
[--enable-termination-protection | --no-enable-termination-protection]
[--cli-input-json <value>]
[--generate-cli-skeleton <value>]
```
