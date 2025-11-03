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

Open the `__main__.py` file from your project directory. This is where you'll define your AWS infrastructure using
Python code.

### Deploy the Pulumi Stack

Deploy the stack using the following command:

```bash
pulumi up
```

Review the proposed changes carefully. Pulumi will show a preview of the resources it will create.

- **Preview:** Displays the resources to be created.
- **Confirmation:** Type "yes" to proceed with the deployment.

### Tear Down the Deployment

To destroy the pulumi stack, navigate to your project directory:

```bash 
cd setup-vpc-in-aws
```

Run the destroy command:

```bash
pulumi destroy
```

Confirm the destruction by typing "yes" when prompted.

If you no longer need the stack, run below command to remove it:

```bash
pulumi stack rm dev
```

### Conclusion

We have successfully set up a VPC with one public subnet, a public route table, and an Internet Gateway
using Pulumi and AWS CLI.