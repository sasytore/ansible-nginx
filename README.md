# Ansible Nginx DevOps Lab

## Overview

This project is a hands-on DevOps laboratory designed to demonstrate infrastructure automation using Ansible, Docker and Nginx.

The project deploys an Nginx container through an Ansible playbook and automatically configures a custom HTML dashboard.

## Architecture

```text
Ansible
   |
   v
Docker
   |
   v
Nginx Container
   |
   v
Custom HTML Dashboard
   |
   v
localhost:8092
