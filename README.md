# DevOps-Project-3tier-Application-Deployment-Tomcat-RabbitMQ-Memcache-MySQL-Azure
![image](https://github.com/kamalmohan217/DevOps-Project-3tier-Application-Deployment-Tomcat-RabbitMQ-Memcache-MySQL-Azure/assets/128888356/62d5b88b-19fd-4cd2-b992-a9403052b834)
Using the Terraform Script present in this repository create the end-to-end Infrastructure.
Using the Terraform Script present in this repository create the end-to-end Infrastructure.
<br><br/>
For RabbitMQ Installation and cluster creation followed below procedure.

**Node-1 (rabbitmq-vm-1)**
![image](https://github.com/kamalmohan217/DevOps-Project-3tier-Application-Deployment-Tomcat-RabbitMQ-Memcache-MySQL-Azure/assets/128888356/6f955d52-9bfd-4079-99d6-85a78cd07179)
![image](https://github.com/kamalmohan217/DevOps-Project-3tier-Application-Deployment-Tomcat-RabbitMQ-Memcache-MySQL-Azure/assets/128888356/314d7b17-c65d-45f9-be7d-dc9b810d2fca)
create user and provide permission to the user.
![image](https://github.com/kamalmohan217/DevOps-Project-3tier-Application-Deployment-Tomcat-RabbitMQ-Memcache-MySQL-Azure/assets/128888356/d0592c6b-6f7c-4500-90b2-2493cc6958a8)
**Node-2 (rabbitmq-vm-2)**
![image](https://github.com/kamalmohan217/DevOps-Project-3tier-Application-Deployment-Tomcat-RabbitMQ-Memcache-MySQL-Azure/assets/128888356/00e671c4-f013-4b05-8190-63d54e2112a3)
![image](https://github.com/kamalmohan217/DevOps-Project-3tier-Application-Deployment-Tomcat-RabbitMQ-Memcache-MySQL-Azure/assets/128888356/9e71fd3f-3040-4d5e-8afb-582e2752a079)
**Node-3 (rabbitmq-vm-3)**
![image](https://github.com/kamalmohan217/DevOps-Project-3tier-Application-Deployment-Tomcat-RabbitMQ-Memcache-MySQL-Azure/assets/128888356/34051d29-4953-46f7-b23b-f5ee7cce65de)
![image](https://github.com/kamalmohan217/DevOps-Project-3tier-Application-Deployment-Tomcat-RabbitMQ-Memcache-MySQL-Azure/assets/128888356/002786c3-6fe2-452c-9324-43adee50ea0b)
**Creation of RabbitMQ Cluster**
**Node-1**
![image](https://github.com/kamalmohan217/DevOps-Project-3tier-Application-Deployment-Tomcat-RabbitMQ-Memcache-MySQL-Azure/assets/128888356/46f9fb03-3085-4afd-9da2-b93eddd62217)
**Node-2**
![image](https://github.com/kamalmohan217/DevOps-Project-3tier-Application-Deployment-Tomcat-RabbitMQ-Memcache-MySQL-Azure/assets/128888356/aa7b0459-55ee-427f-a023-9c768a485065)
**Node-3**
![image](https://github.com/kamalmohan217/DevOps-Project-3tier-Application-Deployment-Tomcat-RabbitMQ-Memcache-MySQL-Azure/assets/128888356/513c1a66-2dce-4ba3-afe8-7016b66cecc1)
![image](https://github.com/kamalmohan217/DevOps-Project-3tier-Application-Deployment-Tomcat-RabbitMQ-Memcache-MySQL-Azure/assets/128888356/6eb137ec-7949-40c0-9c74-ced722c3ac8c)
```
Run below command on Node-1 to set the policy for High Availability (HA) in RabbitMQ Cluster.
rabbitmqctl set_policy ha-all ".*" '{"ha-mode":"all","ha-sync-mode":"automatic"}'
```
Finally copy the Public IP of the Application Gateway of RabbitMQ and create the Record Set in Azure DNS Zone. Access the URL and you will see the default console for RabbitMQ, you can use the initial username and password as guest and login into the RabbitMQ console. 
![image](https://github.com/kamalmohan217/DevOps-Project-3tier-Application-Deployment-Tomcat-RabbitMQ-Memcache-MySQL-Azure/assets/128888356/57a9dab1-64fe-44e4-8bc2-8717f568f234)
<br><br/>
The source code is present in Azure Repos. I have taken the Source Code present in GitHub Repository https://github.com/kamalmohan217/Three-tier-WebApplication.git and did changes in pom.xml, Dockerfile, application.properties as shown below.
![image](https://github.com/kamalmohan217/DevOps-Project-3tier-Application-Deployment-Tomcat-RabbitMQ-Memcache-MySQL-Azure/assets/128888356/96989fe1-cd14-49ed-b3c2-c46b39ee5d29)
![image](https://github.com/kamalmohan217/DevOps-Project-3tier-Application-Deployment-Tomcat-RabbitMQ-Memcache-MySQL-Azure/assets/128888356/7b0310a0-9fb0-4772-897c-ac14909b2c24)
![image](https://github.com/kamalmohan217/DevOps-Project-3tier-Application-Deployment-Tomcat-RabbitMQ-Memcache-MySQL-Azure/assets/128888356/1829d044-a2b1-4a8a-81bf-342ba0e202a6)
![image](https://github.com/kamalmohan217/DevOps-Project-3tier-Application-Deployment-Tomcat-RabbitMQ-Memcache-MySQL-Azure/assets/128888356/b6d9c4ef-e751-487a-b8da-1cde98bea900)
Provide Contibutor Access for Azure Artifacts as shown in screenshot below.
![image](https://github.com/kamalmohan217/DevOps-Project-3tier-Application-Deployment-Tomcat-RabbitMQ-Memcache-MySQL-Azure/assets/128888356/c8970c95-d96b-4cf2-95be-d26808c852cc)
Create a database named as account in mysql and import the file db_backup.sql.
![image](https://github.com/kamalmohan217/DevOps-Project-3tier-Application-Deployment-Tomcat-RabbitMQ-Memcache-MySQL-Azure/assets/128888356/9a447076-ca22-46d0-94ac-f9d6afadadf8)
![image](https://github.com/kamalmohan217/DevOps-Project-3tier-Application-Deployment-Tomcat-RabbitMQ-Memcache-MySQL-Azure/assets/128888356/15b8a2ab-087f-40f2-ba7b-e965bd92f785)
I have created Service Connection for SonarQube and Azure Artifacsts as shown below.
![image](https://github.com/kamalmohan217/DevOps-Project-3tier-Application-Deployment-Tomcat-RabbitMQ-Memcache-MySQL-Azure/assets/128888356/6a6f29a1-8753-4c94-abe8-f2754eb065ce)
<br><br/>
Passwordless Authentication is established between Azure DevOps agent and Tomcat Server (Backend Server).

Now Run the Azure Pipeline (the azure-pipelines.yaml is used as provided with this repository). Create the URL using Public IP for Nginx server after providing an entry for the same in DNS Zone. Access the newly created URL and provide username admin_vp and password admin_vp. 
![image](https://github.com/kamalmohan217/DevOps-Project-3tier-Application-Deployment-Tomcat-RabbitMQ-Memcache-MySQL-Azure/assets/128888356/dcf4cd90-4bd5-4f36-8cdc-ff804baa18b5)
![image](https://github.com/kamalmohan217/DevOps-Project-3tier-Application-Deployment-Tomcat-RabbitMQ-Memcache-MySQL-Azure/assets/128888356/a260f730-18cc-45c1-8355-ded63776e942)
![image](https://github.com/kamalmohan217/DevOps-Project-3tier-Application-Deployment-Tomcat-RabbitMQ-Memcache-MySQL-Azure/assets/128888356/53d38cd4-e2e8-4a17-99aa-ba67f8f0181d)
![image](https://github.com/kamalmohan217/DevOps-Project-3tier-Application-Deployment-Tomcat-RabbitMQ-Memcache-MySQL-Azure/assets/128888356/a2ff6b7b-8526-4fea-9883-dd2144e14c0b)
When you click on the User for the first time it will get the values from MySQL Database and store it in Memcache, so that next time when you click on the same user it will provide the values from the Memcache itself.
![image](https://github.com/kamalmohan217/DevOps-Project-3tier-Application-Deployment-Tomcat-RabbitMQ-Memcache-MySQL-Azure/assets/128888356/172a6aba-ec52-45e7-a8ac-8a5035221f73)
![image](https://github.com/kamalmohan217/DevOps-Project-3tier-Application-Deployment-Tomcat-RabbitMQ-Memcache-MySQL-Azure/assets/128888356/8c0e8a70-5836-4baa-84f3-a58f10a8beac)
After running the Azure Pipeline the Screenshot for RabbitMQ, SonarQube, Azure Artifacts are as shown in the Screenshot below.
![image](https://github.com/kamalmohan217/DevOps-Project-3tier-Application-Deployment-Tomcat-RabbitMQ-Memcache-MySQL-Azure/assets/128888356/15ecf898-4759-4f5e-8b2a-c149706a0d28)
![image](https://github.com/kamalmohan217/DevOps-Project-3tier-Application-Deployment-Tomcat-RabbitMQ-Memcache-MySQL-Azure/assets/128888356/64619c9c-0866-44f9-b2ce-e6f015bff8fd)
![image](https://github.com/kamalmohan217/DevOps-Project-3tier-Application-Deployment-Tomcat-RabbitMQ-Memcache-MySQL-Azure/assets/128888356/2413c6a3-9f1c-455a-8a61-4b5122db89d9)
![image](https://github.com/kamalmohan217/DevOps-Project-3tier-Application-Deployment-Tomcat-RabbitMQ-Memcache-MySQL-Azure/assets/128888356/dab54ac9-46d0-4297-b599-8ed4fe494a8d)
<br><br/>
<br><br/>
<br><br/>
<br><br/>
<br><br/>
<br><br/>
```
Source Code:-  https://github.com/kamalmohan217/Three-tier-WebApplication.git
```
<br><br/>
<br><br/>
<br><br/>
<br><br/>
<br><br/>
<br><br/>
```
Reference:-  https://github.com/logicopslab/vprofile-project.git
```
