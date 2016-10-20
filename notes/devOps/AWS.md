[deployment](deployment.md)

## Amazon Web Services - AWS

### Elastic Compute Cloud - EC2


### Simple Storage Service - S3
CLI:
`aws s3 mb s3://my-first-backup-bucket`: make new bucket
`aws s3 cp fileToUpload.txt s3://my-first-backup-bucket`: copy file to bucket
`aws s3 cp s3://my-first-backup-bucket/fileToUpload.txt ./`: download file from bucket
`aws s3 rm s3://my-first-backup-bucket/fileToUpload.txt`: to delete file from bucket

### Links
[Backup Files to Amazon S3 using the AWS CLI](https://aws.amazon.com/getting-started/tutorials/backup-to-s3-cli/)
