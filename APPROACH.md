# Approach

The primary goal of this assignment was to design a simple, reliable, and reproducible DevOps workflow using industry-standard tools. My approach focused on clarity, automation, and best practices rather than over-engineering the solution.

## Infrastructure Design

I chose **AWS EC2** as the compute platform because it provides a straightforward and transparent way to deploy and expose a containerized application. Since the requirement was to make the application publicly accessible, a public subnet with an internet gateway was sufficient for this use case.

The infrastructure was provisioned using **Terraform** to ensure that all resources (VPC, subnet, security groups, EC2 instance) are defined declaratively and can be recreated consistently across environments. Terraform also makes it easy to manage infrastructure changes and clean up resources when no longer required.

## Containerization Strategy

The Node.js application was containerized using **Docker** to ensure consistency between local development and the production environment. A lightweight official Node.js base image was used to reduce image size and improve startup time.

Docker was installed automatically on the EC2 instance using Terraform `user_data`, which allowed the instance to be ready for application deployment immediately after provisioning.

## CI/CD Approach

**GitHub Actions** was selected for CI because it integrates seamlessly with GitHub and requires no additional setup. The CI pipeline is triggered on every push to the `main` branch and validates the Docker build process.

This ensures that any code changes are automatically checked for build issues before deployment, improving reliability and reducing manual verification.

## Overall Design Philosophy

The overall approach emphasizes:
- Simplicity and clarity
- Infrastructure as Code for repeatability
- Automation wherever possible
- Cost awareness by using Free Tier–eligible resources

This design aligns with real-world DevOps practices while remaining easy to understand and maintain.
