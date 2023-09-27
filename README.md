# aws-operational-tools
Scripts or tools used for aws operational

```bash
$ cd rds_migration_backup_restore
$ virtualenv -p python3 venv
$ source venv/bin/activate

$ pip install boto3

awsudo -u <source-aws-account-profile> -- python3 main.py <source_db_identifier> <destination_arn_of_kms_for_rds> <destination_acc_id> <product_domain>

e.g. creating snapshot from prod db to be used in staging, source = prod AWS account, destination = staging AWS account

awsudo -u sa-pts-prod-kc -- python3 main.py <prod_db_identifier> <stg_RDS_KMS_arn> <stg_acc_id> pts
```

Notes:
- Need to grant access from the source AWS profile to the destination KMS (in the KMS policy).
- source DB should be inside source AWS account.