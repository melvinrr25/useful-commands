#### Add my current public IP to inbound rules on an AWS security rules

```bash
aws ec2 authorize-security-group-ingress --profile ds-staging --group-id sg-xxxxxxxxxxxxxxx --protocol tcp --port 22 --cidr $(dig +short myip.opendns.com @resolver1.opendns.com)/32
```

#### LOOK UP FILES S3  

```bash
aws s3 ls s3://bucket-name --recursive --profile any-profile | egrep "file.txt"
```

#### DOWNLOAD FROM S3

```bash
aws s3 cp s3://bucket-name local-path-to-put-files --recursive --profile any-profile --exclude '*' --include '*any-string*'
```



