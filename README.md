# CloudFormation_Templates

  Cloudformation template to create CI/CD using AWS pipeline that build and deploy to ecs fargate tasks.


## Parameters

### ConnectionArn

The ARN of your Github repo connection.

### GitHubRepo

The name of your repository.

### GitHubBranch

The name of your branch that you want to deploy it.

### Route53HostedZoneName

The name of the hosted zone in AWS that you are going to use it to create a Domain name for your app.

### DomainName

The domain name that you want to connect your app with it.

### S3EnvBucketLocation

Environment variable Bucket Location, Must be the ARN of the S3 bucket. we will store the env variable in S3.

### S3EnvObject

Name of the Environment variable file in the S3 Bucket.

### TemplateBucket

The S3 bucket from which to fetch the templates used by this stack.

## How To Use it

1. Upload these files to AWS S3 bucket.
2. Go to CloudFormation > Create stack > Template is ready > Template source > S3 URL > https://[S3_Bucket_URL]/aws-autostart-pipeline.yaml
3. Set Stack name and the parameters.
4. check `I acknowledge that AWS CloudFormation might create IAM resources with custom names`, and `I acknowledge that AWS CloudFormation might require the following capability: CAPABILITY_AUTO_EXPAND`
5. Create stack.

