# Building Jenkins AMI with Packer Tool
## To create Jenkins AMI please do following steps:

### Create a "json" file based on requested region (e.g "us-east-1.json"). Inside this file please, copy and paste following text:

```
{
    "jenkins_version": "2.235.5-1.1",
    "java_version": "1.8.0",
    "region": "us-east-2",
    "ssh_username": "centos",
    "ssh_keypair_name": "Ansible",
    "ssh_private_key_file": "/home/ec2-user/.ssh/id_rsa"


}
```

### After creating this file, please run following command: 

```
packer build -var-file us-east-1.json jenkins.json
```

