# aws-console
Open the AWS console with your CLI credentials where your needed to be!

## Installation

```
$ brew tap mazerte/software
$ brew install aws-console
```

## Usage

Open the AWS console with your CLI credientials on the Home page

```
$ aws-console
```

Open the AWS console on a specific service
```
$ aws-console s3
```

Open the AWS console on a specific service and region (by default is set to `AWS_DEFAULT_REGION`)
```
$ aws-console ec2 --region eu-west-3
```

Open the AWS console on a specific service with a different profile (by default is set to `AWS_PROFILE`)
```
$ aws-console elb --profile prod
```

## Credientials explainer

When you use `aws-console`, your browser will open and drop the AWS cookies. These cookies will last for `43200 seconds`, so `aws-console` won't recreate new one for `43200 seconds`. If you clear your cookies or log out from the AWS console your can use `--force` flag to force `aws-console` to re-generate a token.

```
$ aws-console route53 --force
```
