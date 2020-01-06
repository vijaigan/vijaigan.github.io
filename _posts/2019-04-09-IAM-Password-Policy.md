---
title: "AWS CLI - IAM Password Policy Update" 

image: 
  path:  /images/aws-cli-password.webp
  thumbnail: /images/aws-cli-password.webp 
categories:
  - AWS 
tags:
  - AWS
  - IAM
  - AWSCLI 
  - SECURITY 
  - PASSWORD 
  - POLICY 
---

To enforce password policy as per your corporate security policy on AWS IAM accounts, please use the following steps.
This will enable setting up password policy for your AWS Account. 


> Please ensure AWS cli is properly configured for your account before you execute the commands.
[AWS CLI Configure](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-configure.html){: .btn .btn--inverse}



~~~shell 

vijai@vijai-lx:~$ #  aws iam update-account-password-policy --minimum-password-length 10 \
		     --require-numbers --require-uppercase-characters \
		     --require-lowercase-characters \
		     --allow-users-to-change-password \ 
 		     --max-password-age 45 

vijai@vijai-lx:~$ aws iam get-account-password-policy --output json 
{
    "PasswordPolicy": {
        "AllowUsersToChangePassword": true, 
        "RequireLowercaseCharacters": true, 
        "RequireUppercaseCharacters": true, 
        "MinimumPasswordLength": 10, 
        "RequireNumbers": true, 
        "RequireSymbols": false, 
        "MaxPasswordAge": 45, 
        "ExpirePasswords": true
    }
}


~~~ 
