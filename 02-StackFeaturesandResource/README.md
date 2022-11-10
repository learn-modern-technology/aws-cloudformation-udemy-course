# Ttitle: Basics of AWS Cloudformation Using YAML
## Description: Learn Basics of AWS Cloudformation to Create AWS Stack and AWS Resources
# 1. Create a Basic Cloud Formation Template using YAML
- Login to AWS Console Management
- Select Stacks on the Left menu options
- This will list all the Stacks that you have uploaded.
- Go to Create Stack (With new Resources) --> Template is Ready -->Upload a Template File
- Select the file and click Next
- Mention the Stack Name and Parameters. Click Next
- Mention the relevant Details and click Next.
- Review all the details and mention create Stack.
- You can check the status of all the resources under Events Tab
- Resources Tab will list all the resources that has been created.
- Template will display the contents of YAML file that was used to create a resource

# 2. Modify the existing Cloud Formation Template and Execute
- Select Stacks on the Left menu options
- This will list all the Stacks that you have uploaded.
- Click on the stack that you already have.
- **Scenario-1:** We can't modify stack that has failed deployment, but we can delete that stack.
- **Scenario-2:** We can update or delete the Stack that has been created successfully.
- **Scenario-3:** For Updating the Stack follow below steps:
                - Click on update stack
                - Select Replace Stack
                - Select Upload template file and upload the file
                - We will follow all the steps as mentioned in Step-01

# 3. Create some more Resources using CloudFormation and use Intrinsic function to use it with another resource
- Create resource - EC2 Instance
- Add Second Resource - New security group and Intrinsic Function Ref
- Update Resource Properties - Add new rule to Security group
- Add third Resource - Elastic IP
- Perform case sensitive test with resource properties

# 4. Intrinsic Function Ref
- The intrinsic function Ref returns the value of the specified parameter or resource.
- Resource Case: When we specify a resource logical name, it returns a value that we can typically use to 
  refer to that resource.
- Parameter Case: When we specify a parameter logical name, it returns the value of that parameter.
Syntax:
    - Long Form
            Ref: logicalName
    - Short Form
            !Ref logicalName
