## VPC with Public and Private Subnets, Route Tables, IGW, and NAT Gateway

We will expand your AWS VPC setup by adding both public and private subnets and configuring Internet access for the
private subnet. Specifically, you will:

- **Create a VPC**
- **Create a Public Subnet**
- **Create a Private Subnet**
- **Set Up an Internet Gateway (IGW)**
- **Create Public and Private Route Tables**
- **Create a NAT Gateway**

### Overview

We will have a VPC with public and private subnets. The public subnet will have direct Internet access, while the
private subnet will have outbound Internet access through a NAT Gateway. This setup is essential for securing resources
while maintaining necessary Internet connectivity.

### Configure AWS CLI

Open your terminal and run the following command to configure your AWS CLI with your credentials:

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

Review the changes that Pulumi will make and confirm by typing `yes`.

**Check the Outputs:**
After the deployment, you should see the exported VPC ID, public subnet ID, private subnet ID, NAT Gateway ID, and route
table IDs in the output.

**Verify in AWS Management Console:**
Go to the AWS Management Console and navigate to the VPC, Subnet, Internet Gateway, and NAT Gateway sections to verify
that the resources have been created as expected.
You can see the resource map in the VPC to check the connection between the resources.

### Destroy

If you want to destroy pulumi resources run below command:
```pulumi destroy```

If you want to completely remove the stack, run below command:
```pulumi stack rm dev```