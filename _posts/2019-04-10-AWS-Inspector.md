---
title: "AWS Inspector - Agent Install"
image: 
  path:  /images/AWS-Inspector-agent-install.webp
  thumbnail: /images/AWS-Inspector-agent-install.webp

categories:
  - AWS 
tags:
  - AWS
  - INSPECTOR
  - AGENT
  - SECURITY 
  - VIDEO
--- 

# Implementation of  AWS Inspector - Agent Install 

## Readings required. 

- [What Is Amazon Inspector?](https://docs.aws.amazon.com/inspector/latest/userguide/inspector_introduction.html){: .btn .btn--inverse}{:target="_blank"}
- [AWS Inspector CLI ](http://docs.aws.amazon.com/cli/latest/reference/inspector/index.html){: .btn .btn--inverse}{:target="_blank"}
- [ AWS Inspector Pricing ](http://aws.amazon.com/inspector/pricing/){: .btn .btn--inverse}{:target="_blank"}
- [Supported OS ](https://docs.aws.amazon.com/inspector/latest/userguide/inspector_supported_os_regions.html){: .btn .btn--inverse}{:target="_blank"}
- [Supported kernel version](https://s3.amazonaws.com/aws-agent.us-east-1/linux/support/supported_versions.json){: .btn .btn--inverse}{:target="_blank"}
>CVE, CIS, or Security Best Practices Rules Packages supports all kernel version.Runtime Behavior Analysis rules package only supports with supported kernel version. 
- [Installing Amazon Inspector Agent](https://docs.aws.amazon.com/inspector/latest/userguide/inspector_installing-uninstalling-agents.html){: .btn .btn--inverse}{:target="_blank"}





~~~shell 
ssh -i key ec2-user@xxxxx 
mkdir inspector ; cd inspector 
wget https://inspector-agent.amazonaws.com/linux/latest/install 
wget https://d1wk0tztpsntt1.cloudfront.net/linux/latest/inspector.gpg -O inspector.key 
gpg --import inspector.key 
curl -O https://d1wk0tztpsntt1.cloudfront.net/linux/latest/install.sig 
gpg --verify ./install.sig 
sudo bash ./install 
~~~ 
- Once the agent install is complete schedule the "run once" assesment from your inspector console. 
- Wait for "Assessment Run" to complete. [ Took about an Hour for me] 
- Download your Assessment Report from [Assessment Run](https://eu-west-1.console.aws.amazon.com/inspector/home?region=eu-west-1#/run) Link as shown in below picture.
![Assessment report](/images/AWS-Inspector-report.webp)

<p>




</P>

### AWS Inspector Agent install video 
<video width="400" height="200" controls preload> 
    <source src="../../video/AWS-Inspector-Agent-install.webm"></source> 
</video

##AWS Inspector Enabling for your account. 

<video width="400" height="200" controls preload> 
    <source src="../../video/inspector.webm"></source> 
</video

