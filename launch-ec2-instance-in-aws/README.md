## Launch EC2 Instances in Public and Private Subnets

We will launch a EC2 instances in both the public and private subnets.

### Configure AWS CLI

Configure the AWS CLI with necessary credentials. Run the following command and follow the prompts to configure it:

`aws configure`

### Set Up a Pulumi Project

Create a new directory for your project and navigate into it and run the following command to initiate and create a new Pulumi project:

```bash
pulumi new aws-python
```

Follow the prompts to set up your project.

**Create a Key Pair:** Run the following command to create a new key pair:

```bash
aws ec2 create-key-pair --key-name MyKeyPair --query 'KeyMaterial' --output text > MyKeyPair.pem
```

**Set File Permissions:**

```bash
chmod 400 MyKeyPair.pem
```

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

### Verify the Deployment

After the deployment completes, you should see the exported VPC ID, public subnet ID, private subnet ID, NAT Gateway ID,
and instance IDs in the output.

### Destroy

If you want to destroy pulumi resources run below command:
```pulumi destroy```

If you want to completely remove the stack, run below command:
```pulumi stack rm dev```