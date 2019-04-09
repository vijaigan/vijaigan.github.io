---
title: "AWS CLI - MFA Enable for a IAM user"

image: 
  path:  /images/aws-cli-mfa.png
  thumbnail: /images/aws-cli-mfa.png 
  caption: "[aws cli mfa ](https://vijaigan.github.io/aws/MFA-Enable-via-AWS-CLI/)"
categories:
  - AWS 
tags:
  - AWS
  - IAM
  - AWSCLI 
  - SECURITY 
  - MFA 
---
I was looking for setting up Virtual MFA for IAM user via cli. 
Came across an example as given below reference site. the example given in the reference site uses QRCodePNG.
I wanted to use Base32StringSeed as option check how it works. 

The following command creates virtual mfa device with the name VijaiMFADevice and outputs the string 
to a file called mfa-out. 

Keep in mind that this cli has output option of either QRCodePNG or Base32StringSeed. 
I have choosen Base32StringSeed as example.  
{: .notice}

[aws iam create-virtual-mfa-device ](https://docs.aws.amazon.com/cli/latest/reference/iam/create-virtual-mfa-device.html){: .btn .btn--inverse}

~~~shell 
vijai@vijai-lx:~/AWS$ aws iam create-virtual-mfa-device    \ 
--virtual-mfa-device-name VijaiMFADevice --outfile mfa-out \ 
--bootstrap-method Base32StringSeed

VIRTUALMFADEVICE    arn:aws:iam::636XXXXXXX:mfa/VijaiMFADevice
~~~ 

1. Now the `mfaout` file has Base32String.
2. Open google autheticator and add new with + sign 
3. Choose "Enter Provided Key" 
4. This will ask for new account name and "Your Key" 
5. Please input the whole string from mfaout as input. 
6. Note down consecutive 2 Number's from google authenticator 
7. Use the following AWS CLI for setting up MFA token sync. 

[aws iam enable-mfa-device ](https://docs.aws.amazon.com/cli/latest/reference/iam/enable-mfa-device.html){: .btn .btn--inverse}
~~~shell 
vijai@vijai-lx:~/AWS$ aws iam enable-mfa-device --user-name vijai@XXXXX \ 
--serial-number "arn:aws:iam::63XXXXXXXXX:mfa/VijaiMFADevice" \ 
--authentication-code1 12345 \
--authentication-code2 12345 
~~~ 

That's it. 

You have enabled Virtual MFA for your IAM account. Now if you login to the console, you will be asked for MFA Token .

### Reference site 

https://typicalrunt.me/2018/05/26/enabling-an-aws-iam-mfa-via-cli/  
