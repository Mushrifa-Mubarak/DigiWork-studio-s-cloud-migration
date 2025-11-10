#DigiWorks Studio Cloud Migration

This repository contains the infrastructure automation project for DigiWorks Studio, designed and implemented by Muneeba Mubarak. The project focuses on migrating DigiWorks Studio's legacy infrastructure to AWS Cloud using Infrastructure as Code (IaC) principles via AWS CloudFormation.

## Project Overview
DigiWorks Studio is a digital agency facing challenges with scalability, security, and operational efficiency. This project addresses those challenges by:
- Migrating legacy systems to AWS
- Applying the AWS 7R Migration Framework
- Automating infrastructure deployment using CloudFormation

## Migration Strategy
The migration strategy is based on the AWS 7R Framework:
- *Rehost*: Web Servers → Amazon EC2
- *Replatform*: Database → Amazon RDS
- *Repurchase*: Firewall → AWS Security Groups
- *Replace*: Email → Amazon WorkMail
- *Retain*: Active Directory (Phase 2)
- *Refactor*: Backup System → AWS Backup

## Architecture Highlights
- Multi-tier architecture across multiple Availability Zones
- VPC with public/private subnets
- EC2 instances with Auto Scaling and Load Balancer
- RDS MySQL with automated backups
- S3 buckets for media and backup storage
- IAM roles and Security Groups for access control
- CloudWatch for monitoring and alerting

## Files Included
- digiworks-master.yaml: CloudFormation template for deploying the infrastructure
- README.md: Project documentation and overview

## AWS Well-Architected Framework
The design aligns with the AWS Well-Architected Framework:
- *Operational Excellence*: IaC, monitoring, automated backups
- *Security*: IAM, encryption, access control
- *Reliability*: Multi-AZ, failover, backups
- *Performance Efficiency*: Right-sized instances, auto scaling
- *Cost Optimization*: Free-tier usage, lifecycle policies
