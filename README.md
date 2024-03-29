# aws-cli

```
aws iam list-users
```
```
aws ec2 create-key-pair --key-name aws-sreejith --query 'KeyMaterial' --output text > ~/.ssh/aws-sreejith.pem
```
```
aws ec2 describe-key-pairs --key-name aws-sreejith.pem
```
```
aws ec2 delete-key-pair --key-name aws-sreejith.pem
```
```
aws ec2 create-security-group --group-name sreejith_SG_useast1 --description 'Security group for sreejith and us east 1'
```
```
aws ec2 describe-security-groups --group-id sg-324324
```
```
aws ec2 authorize-security-group-ingress --group-id sg-234324 --protocol tcp --port 22 --cidr 0.0.0.0/0
```
```
aws ec2 authorize-security-group-ingress --group-id sg-234324 --protocol tcp --port 5432 --cidr 0.0.0.0/0 --source-group sg-234324
```
```
aws ec2 delete-security-group --group-id sg-234234
```
```
aws ecs create-cluster --cluster-name deepdive
```
```
aws ecs list-clusters
```
```
aws ecs describe-clusters --clusters deepdive
```
```
aws ecs delete-cluster --cluster deepdive
```
```
aws s3api create-bucket --bucket sreejithgp_deepdive
```
```
aws s3 cp ecs.config s3://sreejithgp_deepdive/ecs.config
```
```
aws s3 ls s3://sreejithgp_deepdive
```
```
aws ec2 run-instances --image-id ami-2b3b6041 --count 1 --instance-type t2.micro --iam-instance-profile Name=ecsInstanceRole --key-name aws-sreejith --security-group-id sg-324234 --user-data file://copy-ecs-config-to-s3
```
```
aws ec2 describe-instance-status --instance-id i-234234
```
```
aws ecs list-container-instances --cluster deepdive
```
```
aws ecs describe-container-instances --cluster deepdive --container-instances container-instance-arms-value
```
```
aws ec2 terminate-instances --instance-ids i-324234
```
