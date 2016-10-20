[deployment](deployment.md)

## [Amazon Web Services - AWS](https://aws.amazon.com/)
[Wikipedia](https://en.wikipedia.org/wiki/Amazon_Web_Services)

### Elastic Beanstalk
- [Getting Started with Web App Deployment on Elastic Beanstalk](https://docs.aws.amazon.com/quickstarts/latest/webapp/welcome.html?icmpid=docs_eb_console_new)

### [Elastic Compute Cloud - EC2](https://aws.amazon.com/ec2/)
[Wikipedia](https://en.wikipedia.org/wiki/Amazon_Elastic_Compute_Cloud)

### Simple Storage Service - S3
[Wikipedia](https://en.wikipedia.org/wiki/Amazon_Simple_Storage_Service)

#### CLI:
- `aws s3 mb s3://my-first-backup-bucket`: make new bucket
- `aws s3 cp fileToUpload.txt s3://my-first-backup-bucket`: copy file to bucket
- `aws s3 cp s3://my-first-backup-bucket/fileToUpload.txt ./`: download file from bucket
- `aws s3 rm s3://my-first-backup-bucket/fileToUpload.txt`: to delete file from bucket

### Links
- [Backup Files to Amazon S3 using the AWS CLI](https://aws.amazon.com/getting-started/tutorials/backup-to-s3-cli/)
- [Installing the AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/installing.html#install-bundle-other-os)
