# Upload-Artifacts-to-s3

1. Create a S3 bucket in aws.
2. Create an IAM User with "AmazonS3FullAccess" policy.
3. Install S3 Publisher Plugin in your jenkins.
4. In "Manage Jenkins" -> "Configure Settings" -> "Amazon S3 profiles", enter "Access key" and "Secret key" of that IAM user.
