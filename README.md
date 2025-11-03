## Learning Pulumi with AWS

This repository is created for the purpose of learning and practicing Pulumi concepts and how they apply to AWS. It
contains various Pulumi configurations for provisioning resources and managing infrastructure on AWS.

### Introduction

**Pulumi** is an open-source infrastructure as code (IaC) tool that allows you to define, provision, and manage cloud
resources using **familiar programming languages** like TypeScript, Python, Go, and C#. In this repository, we explore
how to use Pulumi to interact with AWS, including setting up networks, EC2 instances, databases, S3 buckets, and more.

### Prerequisites

Before you start using Pulumi with AWS, ensure you have the following installed and configured:

- [Pulumi CLI](https://www.pulumi.com/docs/install/)
- A programming language runtime (e.g., [Node.js](https://nodejs.org/), [Python](https://www.python.org/))
- [AWS CLI](https://aws.amazon.com/cli/)
- [An AWS Account](https://aws.amazon.com/)

Additionally, set up your AWS credentials by configuring the AWS CLI:

```bash
aws configure
```

### Getting Started

Clone this repository:

```bash
git clone [https://github.com/minhajul/learning-pulumi.git](https://github.com/minhajul/learning-pulumi.git)
cd learning-pulumi
```

Change to a specific project folder. Follow the project specific `readme.md` to provision the resources on AWS:

### Usage

- **Creating Resources:** To create or update resources, simply use the `pulumi up` command from within any of the
  subdirectories. Modify the source code files to suit your needs.
- **Stack Outputs:** Once the configuration is applied, Pulumi will display any exported stack outputs, such as an EC2
  instance's public IP, S3 bucket URL, etc.
- **Configuration and Customization:** Customize your stack's configuration using `pulumi config set <key> <value>.`
  This is
  an alternative to hardcoding values and is useful for setting the AWS region, instance sizes, or other parameters.

### Notes

- Always be careful when running` pulumi up` on your AWS account. Some resources can incur costs, such as EC2 instances
  and RDS databases.
- Use the `pulumi destroy` command to remove resources after experimentation or when they are no longer needed to avoid
  unnecessary charges.

### Contributing

Feel free to fork this repository, make changes, and submit pull requests. This project is primarily for educational
purposes, so if you encounter any issues, please open an issue, and we will work on resolving it.

### Made with ❤️ by [[minhajul](https://github.com/minhajul)]