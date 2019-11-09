## Add my current public IP to inbound rules on an AWS security rules

```bash
aws ec2 authorize-security-group-ingress --profile ds-staging --group-id sg-xxxxxxxxxxxxxxx --protocol tcp --port 22 --cidr $(dig +short myip.opendns.com @resolver1.opendns.com)/32
```
