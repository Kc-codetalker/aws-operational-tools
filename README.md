# aws-operational-tools
Scripts or tools used for aws operational

$ cd rds_migration_backup_restore
$ virtualenv -p python2 venv
$ source venv/bin/activate

$ pip install boto3

awsudo -u <source-aws-account-profile> -- python2 main.py <source_db_identifier> <destination_arn_of_kms_for_rds> <destination_acc_id> <product_domain>