# packer-nginx-AWS
Create a nginx EBS AMI on AWS with Packer


## Pre-requesties

* [Packer](https://www.packer.io/downloads)


## How to use this repo

- Clone
- Build
- Clean up

---

### Clone the repo

```
git clone https://github.com/ayahmuhamed/packer-nginx-AWS
```

### Change directory

```
cd packer-aws-nginx
```

### Validate the template

```
packer validate aws-ubuntu.pkr.hcl
```

### AWS login


export AWS credentials
```
export AWS_ACCESS_KEY_ID="aws_access_key_id"
export AWS_SECRET_ACCESS_KEY="aws_secret_access_key"
export AWS_SESSION_TOKEN="aws_session_token"
```


### Build the image

```
packer build aws-ubuntu.pkr.hcl
```

### Clean up/ Derigester created Image

- Go to AWS Console (Okta > Doormat App) in a webbrowser
- Go to EC2 > AMI 
-  Select the Image name (aws-ubuntu.pkr)AMI > Actions > Deregister
     <img width="1538" alt="Screenshot 2021-09-07 at 16 22 10" src="https://user-images.githubusercontent.com/88331884/132361293-364a04f5-6245-4f2b-8181-bcea6486b371.png">
