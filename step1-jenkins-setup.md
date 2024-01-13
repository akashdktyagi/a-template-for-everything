### 1. Set up Jenkins server on AWS

* I am using Bitnami Jenkins here. You have a resuable AMI which bitnami provides and you can directly use it. 
* Recommended server size is t3a.small which gives you 2 Core and 2 gig of RAM.
* Creating an instance is out of scope but make sure you set it up in your default VPC and the security group you are using allows TCP traffic. If you do not know it yet, I would recommend go through some decent tutorial on how to spin up an EC2 instance in AWS. There are plenty of resources online for that.
* Notice the AMI I am using in below screen shot: ```bitnami-jenkins-2.426.2-0-linux-debian-11-x86_64-hvm-ebs-nami-447af561-b7e2-4d03-8a67-4842db5439cb```

* ![Alt text](ss/image.png)

* Once you have the instance up and running navigate to the public url of your server and it should serve the jenkins login page.
* Username is : ```user``` but password has to be retrieved. Instructions on how to retrieve the password is listed here: https://docs.bitnami.com/aws/faq/get-started/find-credentials/

* After login go to settings and add below plugins:
    * git
    * pipeline
    * docker
    * Note: When you search for these plugins you will see lot of plugins with similar title. Just install the plugins with the simple titles as above.

* Restart the Jenkins
