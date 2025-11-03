## Setting Up a VPC Using Pulumi and AWS CLI

A VPC is a virtual network dedicated to AWS account, where you can launch AWS resources in a logically isolated section
of the AWS Cloud. We will step by step create a VPC with a public subnet, configuring the necessary components using Pulumi python.

**The tasks include:**
1. **Creating a VPC
2. **Creating a Public Subnet
3. **Creating an Internet Gateway (IGW)
4. **Creating a Public Route Table

### Configure AWS CLI

Configure the AWS CLI with necessary credentials. Run the following command and follow the prompts to configure it:

```bash 
aws configure
```

### Set Up a Pulumi Project

**Initialize a New Pulumi Project:**

We will here use `pulumi` `python`. Run the following command to create a new Pulumi project:

```bash
pulumi new aws-python
```

Follow the prompts to set up your project.

### Create the Pulumi Program

Copy the `__main__.py` file in your project directory. This is where you will write the code to define your AWS
infrastructure.

### Deploy the Pulumi Stack

Deploy the stack using the following command:

```bash
pulumi up
```

Review the proposed changes carefully. Pulumi will show a preview of the resources it will create.

- **Preview:** Displays the resources to be created.
- **Confirmation:** Type "yes" to proceed with the deployment.

### Destroy

If you want to destroy pulumi resources run below command:
```pulumi destroy```

If you want to completely remove the stack, run below command:
```pulumi stack rm dev```