# awsecr

Getting started with Amazon ECR using the AWS CLI
https://docs.aws.amazon.com/AmazonECR/latest/userguide/getting-started-cli.html


Configure ECS for EC2
https://www.lynda.com/Docker-tutorials/Configure-ECS-EC2/2811348/2930442-4.html?srchtrk=index%3a14%0alinktypeid%3a2%0aq%3aaws%0apage%3a1%0as%3arelevance%0asa%3atrue%0aproducttypeid%3a2



ssh -i "ecr20200620.pem" ec2-user@ec2-54-252-128-18.ap-southeast-2.compute.amazonaws.com

      __|  __|_  )
       _|  (     /   Amazon Linux 2 AMI
      ___|\___|___|

https://aws.amazon.com/amazon-linux-2/
4 package(s) needed for security, out of 10 available
Run "sudo yum update" to apply all updates.
[ec2-user@ip-10-0-0-158 ~]$ sudo yum



http://ec2-54-252-128-18.ap-southeast-2.compute.amazonaws.com/
Hello World!

https://ecsworkshop.com/
https://www.eksworkshop.com/
https://aws.amazon.com/getting-started/hands-on/build-modern-app-fargate-lambda-dynamodb-python/module-two/



Login Succeeded
[ec2-user@ip-10-0-0-158 ~]$ docker push 916461470826.dkr.ecr.ap-southeast-2.amazonaws.com/hello-world:latest
The push refers to repository [916461470826.dkr.ecr.ap-southeast-2.amazonaws.com/hello-world]
792a831d0217: Pushed
7f3e21a4e693: Pushed
7547faaeb56a: Pushed
ddc500d84994: Pushed
c64c52ea2c16: Pushed
5930c9e5703f: Pushed
b187ff70b2e4: Pushed
latest: digest: sha256:56b974f92b9304c672531e38fe89aec75f5240528418249fb3a43d7e459adc66 size: 1778


916461470826.dkr.ecr.ap-southeast-2.amazonaws.com/hello-world:latest

latest: digest: sha256:56b974f92b9304c672531e38fe89aec75f5240528418249fb3a43d7e459adc66 size: 1778
[ec2-user@ip-10-0-0-158 ~]$ docker pull 916461470826.dkr.ecr.ap-southeast-2.amazonaws.com/hello-world:latest
latest: Pulling from hello-world
Digest: sha256:56b974f92b9304c672531e38fe89aec75f5240528418249fb3a43d7e459adc66
Status: Image is up to date for 916461470826.dkr.ecr.ap-southeast-2.amazonaws.com/hello-world:latest
916461470826.dkr.ecr.ap-southeast-2.amazonaws.com/hello-world:latest
[ec2-user@ip-10-0-0-158 ~]$ aws ecr batch-delete-image \
>       --repository-name hello-world \
>       --image-ids imageTag=latest
{
    "failures": [],
    "imageIds": [
        {
            "imageTag": "latest",
            "imageDigest": "sha256:56b974f92b9304c672531e38fe89aec75f5240528418249fb3a43d7e459adc66"
        }
    ]

