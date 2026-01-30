MD

\#AWS EC2 + Nginx Setup



\## Objective

Deploy an Amazon Linux EC2 instance and host a web server using Nginx.



\## Steps

1. Launched EC2 (Amazon Linux 2023
2. Configured key pair and security group
3. Connected via SSH
4. Install and enabled Nginx



\## Commands

```bash

sudo yum update -y

sudo yum install nginx -y

sudo systemctl start nginx

sudo systemctl enable nginx



\## Result

Successfully accessed the Nginx default page using the EC2 public IP.

