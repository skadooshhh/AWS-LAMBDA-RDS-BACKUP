# AWS-LAMBDA-RDS-BACKUP
lamda function to take RDS backup on different accounts for DR strategy.
Two lambda functions:
* AWS-RDS-COPY for taking manual backups
* AWS-RDS-SHARE for Sharing this backup to child account or any other account.

Before creating lambda function understanding on below topics is suggested:
* Autobackups
* Manual backups
* KMS Key ID

Function handles: 
 1. Takes manual copy from Auto Backups of a given RDS instance Identifier.
    Note: Taking manual copy from Autobackups is suggested as it is faster and has delta. 
 2. If No autobackups enabled for a given instance, create backup on a RDS identifier is executed.
 3. If different KMS key ID enabled for a  RDS INSTANCES, All instances will be encrypted with common KMS key ID snapshot.

# PRE-REQUISITE
* IAM Role policy for lambda function





