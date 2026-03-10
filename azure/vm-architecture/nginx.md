# Nginx Web Server - Azure Linux VM

## Overview
Nginx was installed and configured on an Ubuntu Linux virtual machine to validate inbound HTTP traffic NSG rules and VM connectivity.

## Installation
Nginx was installed using the default Ubuntu package manager.


```bash

sudo apt update

sudo apt install nginx -y

sudo systemctl start nginx

sudo systemctl enable nginx

