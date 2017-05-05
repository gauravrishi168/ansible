# awsbackup.yml

This is an awsbackup.yml playbook.  
Example run:

```
ansible-playbook -i inventory/localhost awsbackup.yml -e "INCREMENTAL=daily COUNT=3"
```

# AWS policy

The following is the AWS policy used to run this playbook.

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "ec2:CreateSnapshot",
                "ec2:CreateTags",
                "ec2:DeleteSnapshot",
                "ec2:CreateVolume",
                "ec2:Describe*"
            ],
            "Resource": [
                "*"
            ]
        }
    ]
}
```
