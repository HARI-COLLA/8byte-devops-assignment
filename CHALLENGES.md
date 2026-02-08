# Challenges and Resolutions

During the implementation of this assignment, I encountered a few practical challenges that are common in real-world DevOps workflows. Each issue was resolved through troubleshooting and applying best practices.

## Terraform Directory and Git Issues

Initially, the Terraform `.terraform` directory and provider binaries were accidentally committed to the Git repository. This caused GitHub to reject the push due to large file size limits.

**Resolution:**  
I added a `.gitignore` file to exclude Terraform cache files and removed the provider binaries from Git history. This reinforced the importance of keeping local Terraform artifacts out of version control.

## Region-Specific Instance Type Limitation

While deploying the EC2 instance in the `ap-south-2` region, the `t2.micro` instance type was not eligible for the Free Tier, which caused the deployment to fail.

**Resolution:**  
I updated the instance type to `t3.micro`, which is Free Tier eligible in the selected region. This highlighted the need to consider region-specific limitations when designing cloud infrastructure.

## GitHub README Formatting Issues

While documenting the project, Markdown formatting issues occurred due to incorrect use of quotation marks instead of backticks for code blocks, which caused the README to render incorrectly.

**Resolution:**  
I corrected the formatting by using proper Markdown syntax and validated the output using GitHub’s preview feature before committing changes.

## Cost Management Considerations

Keeping an EC2 instance running continuously can incur costs after Free Tier limits are exceeded.

**Resolution:**  
The infrastructure was designed to be easily stoppable or destroyable using Terraform. Screenshots and documentation were included to allow verification even if the instance is stopped after evaluation.

## Key Learnings

These challenges helped reinforce:
- The importance of clean version control practices
- Awareness of cloud provider limitations
- Proper documentation techniques
- Cost-conscious infrastructure management
