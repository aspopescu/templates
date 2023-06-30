# AWS RDS Terraform Module

This module creates an Amazon S3 (Object Storage) instance on AWS (Amazon Web Services).

## Prerequisites

- Terraform v0.14.0 or newer
- An AWS account

## Usage

To use this module, you'll need to provide values for the following variables:

- `bucket_name`: The name of the bucket.

## Outputs

The module will output the following:

- `s3_bucket_name`: The name of the created bucket.
- `s3_bucket_region`: The region of the created bucket.

## Further Steps

It would be best for you to create an IAM user also for the application, which only has permissions to read and write files into the bucket.

## Run `terraform apply`

```bash
terraform apply --auto-approve \
  -var "bucket_name=your-bucket-name"
```

## IAM permissions

You will need a user with a policy containing the following permissions to run this module:
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "VisualEditor0",
      "Effect": "Allow",
      "Action": [
        "s3:GetObjectVersionTagging",
        "s3:CreateBucket",
        "s3:GetStorageLensConfigurationTagging",
        "s3:GetObjectAcl",
        "s3:GetBucketObjectLockConfiguration",
        "s3:DeleteBucketWebsite",
        "s3:GetIntelligentTieringConfiguration",
        "s3:GetObjectVersionAcl",
        "s3:PutBucketAcl",
        "s3:DeleteObject",
        "s3:GetBucketPolicyStatus",
        "s3:GetObjectRetention",
        "s3:GetBucketWebsite",
        "s3:GetJobTagging",
        "s3:GetMultiRegionAccessPoint",
        "s3:GetObjectAttributes",
        "s3:GetObjectLegalHold",
        "s3:GetBucketNotification",
        "s3:PutBucketCORS",
        "s3:DescribeMultiRegionAccessPointOperation",
        "s3:GetReplicationConfiguration",
        "s3:PutObject",
        "s3:GetObject",
        "s3:DescribeJob",
        "s3:GetAnalyticsConfiguration",
        "s3:GetObjectVersionForReplication",
        "s3:GetAccessPointForObjectLambda",
        "s3:GetStorageLensDashboard",
        "s3:GetLifecycleConfiguration",
        "s3:GetAccessPoint",
        "s3:GetInventoryConfiguration",
        "s3:GetBucketTagging",
        "s3:PutAccelerateConfiguration",
        "s3:GetAccessPointPolicyForObjectLambda",
        "s3:GetBucketLogging",
        "s3:ListBucket",
        "s3:GetAccelerateConfiguration",
        "s3:GetObjectVersionAttributes",
        "s3:GetBucketPolicy",
        "s3:GetEncryptionConfiguration",
        "s3:GetObjectVersionTorrent",
        "s3:GetBucketRequestPayment",
        "s3:GetAccessPointPolicyStatus",
        "s3:GetObjectTagging",
        "s3:GetMetricsConfiguration",
        "s3:GetBucketOwnershipControls",
        "s3:DeleteBucket",
        "s3:GetBucketPublicAccessBlock",
        "s3:GetMultiRegionAccessPointPolicyStatus",
        "s3:PutBucketPublicAccessBlock",
        "s3:GetMultiRegionAccessPointPolicy",
        "s3:GetAccessPointPolicyStatusForObjectLambda",
        "s3:PutBucketOwnershipControls",
        "s3:GetBucketVersioning",
        "s3:GetBucketAcl",
        "s3:GetAccessPointConfigurationForObjectLambda",
        "s3:GetObjectTorrent",
        "s3:GetMultiRegionAccessPointRoutes",
        "s3:GetStorageLensConfiguration",
        "s3:GetAccountPublicAccessBlock",
        "s3:GetBucketCORS",
        "s3:GetBucketLocation",
        "s3:GetAccessPointPolicy",
        "s3:GetObjectVersion",
        "s3:PutAccessPointConfigurationForObjectLambda",
        "s3:PutBucketObjectLockConfiguration",
        "s3:PutObjectAcl",
        "s3:PutObjectVersionAcl"
      ],
      "Resource": "*"
    }
  ]
}
```
