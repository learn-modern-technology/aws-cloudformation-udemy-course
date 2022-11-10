# Ttitle: Parameters in AWS Cloudformation Using YAML
## Description: Learn Basics of AWS Cloudformation - How we can leverage Conditions on AWS

# 1. Intro about Conditions
- Conditions are evaluated based on predefined Psuedo parameters or input parameter values that we specify when we 
  create or update stack.
- Within each condition we can reference the other condition.
- We can associate these conditions in three places.
  - Resources
  - Resource Properties
  - Outputs
- At stack creation or stack update, AWS CloudFormation evaluates all conditions in our template. During stack 
  update, Resources that are now associated with a false condition are deleted.
- Important Note: During stack update, we cannot update conditions by themselves. We can update conditions only when 
  we include changes that add, modify or delete resources

# 2. Conditions - Intrinsic Functions
## Conditions Properties
We can use the below listed intrinsic functions to define conditions in cloud formation template.
- Fn::And
- Fn::Equals
- Fn::If
- Fn::Not
- Fn::Or

# 3. What we are going to do using Conditions
1. Create an EIP when environment is prod, use intrinsic function Fn::Equals
2. Create a security group for dev environment when condition is met and demonstrate Pseudo parameter “AWS::NoValue” 
   for when environment is prod. Use Intrinsic function Fn::If
3. Create a security group for prod env with prod related condition added. Use Intrinsic function Fn::If
4. How to use Intrinsic function Fn::Not
5. How to use Intrinsic function Fn::Or
6. How to use Intrinsic function Fn::And