# aws-apprunner

App Runner is a fully managed service that makes it easy to deploy web applications and APIs at scale

No infrastructure experience required

Start with your source code or container image

It automatically builds and deploy the web app

App Runner provides Automatic scaling, highly available, load balancer, encryption

App Runner can Connect to database, cache, and message queue services

**Use cases:** web apps, APIs, microservices, rapid production deployments

**Create a App Runner with Amazon public container registry**

To do so, first create a source for App Runner service. Here, I'm going to select container image with Amazon Public Repository,

![image](https://github.com/kohlidevops/aws-apprunner/assets/100069489/5528cbd3-db5e-4699-a244-28b9e752b6ea)

This is Amazon Public Repository link to explore and pick your container image.

**https://gallery.ecr.aws/**

Deployment should be a Manual when you go with Amazon Public Repository Container image

![image](https://github.com/kohlidevops/aws-apprunner/assets/100069489/4862cf6f-4b7a-430e-9f4b-8476e36c008f)

Here is the configuration for your services such as CPU and Memory. Even you can add the Environment variables which is more secure than hardcoded secrets in image. Right!

Im using httpd image for AppRunner. So I can go with Port 80.

![image](https://github.com/kohlidevops/aws-apprunner/assets/100069489/a2aca5e3-b279-4b4a-a22c-dbaa54ebb522)

For Autoscaling, we can do either Automatic or Manual.

![image](https://github.com/kohlidevops/aws-apprunner/assets/100069489/de242fbe-0dc2-4f33-abc6-461d17659ddf)

The Loadbalancer health check should configure here depends on your application requirement.

![image](https://github.com/kohlidevops/aws-apprunner/assets/100069489/320ed934-bdfe-4688-8d8d-bd5afcab29bb)

Networking configuration simply about your Incoming and Outgoing Networking Traffic. You can even go with Private ebdpoint if you are configured Private Link and you can select custom VPC in Outgoing to send traffic to any endpoint (Private or Public endpoint).

![image](https://github.com/kohlidevops/aws-apprunner/assets/100069489/70db8ec0-c739-4143-838d-1240890263ce)

Then review and deploy the App Runner. Here we go, its Running state. 

![image](https://github.com/kohlidevops/aws-apprunner/assets/100069489/77ce8adb-830d-4220-bf91-94210e5fd4a3)

You can access the application using default domain. Perfect, its working as we expected.

![image](https://github.com/kohlidevops/aws-apprunner/assets/100069489/9211df4a-cb0d-4fb1-a049-d0c550a94d12)

Once App Runner has been created, You can check all the logs with in AWS console. Thats really beauty.

![image](https://github.com/kohlidevops/aws-apprunner/assets/100069489/d39e7f1c-850f-49bc-bc6d-7ab945bcf007)

You can check the metrics such as Request Count, HTTP response count, Request latency, CPU , Memory utilization and so on.

![image](https://github.com/kohlidevops/aws-apprunner/assets/100069489/4f20c0f7-4d30-42f9-bfc6-689ced9ebfe8)

In Configuration, you can change the repository, images, deployment type - manual or automatic, Helath check and so on.

![image](https://github.com/kohlidevops/aws-apprunner/assets/100069489/909822cd-ca18-407d-85c3-908474cfc56d)

Even you can link with custom domain too.

![image](https://github.com/kohlidevops/aws-apprunner/assets/100069489/a74a5ca5-4e0c-403e-865f-29275797c0b8)

That's it. 


