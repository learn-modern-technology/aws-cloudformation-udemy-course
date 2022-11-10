# Ttitle: Parameters in AWS Cloudformation Using YAML
## Description: Learn Basics of AWS Cloudformation - How we can leverage Parameters in AWS

# 1. Intro about Parameters
- Parameters: Parameters enable us to input custom values to our template each time when we create or update stack.
- We can have maximum of 60 parameters in a cfn template.
- Each parameter must be given a logical name (logical id) which must be alphanumeric and unique among all logical 
  names within the template.
- Each parameter must be assigned a parameter type that is supported by AWS CloudFormation.
- Each parameter must be assigned a value at runtime for AWS CloudFormation to successfully provision the stack. We 
  can optionally specify a default value for AWS CloudFormation to use unless another value is provided.
- Parameters must be declared and referenced within the same template. 
- We can reference parameters from the Resources and Outputs sections of the template
- Example of Syntax

# 2. Some of the Properties of Parameters are given below.
## Parameter Properties
- AllowedPattern
- AllowedValues
- ConstraintDescription
- Default
- Description
- MaxLength
- MaxValue
- MinLength
- MinValue
- NoEcho

## Parameter Types
1. Type (Mandatory)
2. String
3. Number
4. List<Number>
5. CommaDelimitedList
6. AWS Specific
        - AWS::EC2::Instance::Id
        - AWS::EC2::VPC::Id
        - List<AWS::EC2::Subnet::Id>
7. SSM Parameter Type
        - AWS::SSM::Parameter::Name
        - AWS::SSM::Parameter::Value<String>
        - AWS::SSM::Parameter::Value<List<String>>

# 3. What we are going to do using Parameters
1. Create a parameter type of AWS for KeyName property of ec2 instance.
2. Create a parameter type of string for AvailabilityZone property of ec2 instance.
3. Create a parameter type of string for InstanceType property of ec2 instance.
4. (Pre-requisite) Create a SSM Parameter in parameter store.
     Create a parameter type of SSM for InstanceType property of ec2 instance.


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
