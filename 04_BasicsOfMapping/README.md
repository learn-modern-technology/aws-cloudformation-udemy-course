# Ttitle: Parameters in AWS Cloudformation Using YAML
## Description: Learn Basics of AWS Cloudformation - How we can leverage Mappings on AWS

# 1. Intro about Mappings
- Mappings section matches a key to a corresponding set of named values.
- For example, if we want to set values based on a region, we can create a mapping that uses region name as a key and 
  contains the values we want to specify for each region.
- We can use Fn::FindInMap intrinsic function to retrieve values in map
- The intrinsic function FindInMap returns the value corresponding to keys in a two-level map that is declared in 
  Mappings section

# 2. Some of the Properties of Mappings are given below.
## Mappings Properties
- Map Name
- Top Level Key
- Second Level Key
- Return Value

# 3. What we are going to do using Mappings
1. Create a Mapping to select the AMI ID for ec2 instance property – ImageId based on region.
    - Top Level Key: Region (us-east-2, us-west-1)
    - Second Level Key: AmiId
2. Create a Mapping to select the instance type based on environments (dev or prod) for ec2 instance property - 
    InstanceType
    - Top Level Key: Environment (dev, prod)
    - Second Level Key: Instance Type

# 4. Pseudo Parameters
1. Pseudo parameters are parameters that are predefined by AWS CloudFormation.
2. We don’t need to declare them in our template.
3. We can use them the same way as we use parameters as an argument for Ref function.
Some Psudo Paramters that we will use in Cloud Formation Template
•AWS::AccountId
•AWS::NotificationARNs
•AWS::NoValue
•AWS::Partition
•AWS::Region
•AWS::StackId
•AWS::StackName
•AWS::URLSuffix