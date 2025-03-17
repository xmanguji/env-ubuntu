# ubunt-environment

## Activate & Install & env create with python version
```
source .venv/bin/activate
pip install -r requirements.txt
virtualenv .venv --python=python3.8
virtualenv .denv --python=python3.8
```
## Ec2 Launch
 1. Allow your IP Address in Ec2 Security Group
 2. Using Putty
    - Pem file Create 
    - pwd: Ubuntu
    - port: 22
    - Connection/SSH/Auth/Credentials / PPK load

## http to https (Let's encrypt)
https://www.digitalocean.com/community/tutorials/how-to-secure-nginx-with-let-s-encrypt-on-ubuntu-22-04

## Finding the path
 - cd ..
 - cd ..
 - ls
 - cd var/www/tokenlite/ICO

## Deploy Laravel App to Amazon EC2 (Ngnix)
https://dev.to/chengkangzai/set-by-step-how-to-deploy-laravel-app-to-amazon-ec2-free-tier-4ca8

## Docker push
```
docker build -t tst . --platform=linux/amd64
docker tag tst:latest 701494763670.dkr.ecr.us-east-1.amazonaws.com/report-api:latest
aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin 701494763670.dkr.ecr.us-east-1.amazonaws.com
aws s3 sync static/ s3://respro-android-staging/static --region=us-east-1
docker push 701494763670.dkr.ecr.us-east-1.amazonaws.com/report-api:latest

```
