# Update aws ssm parameters using github actions workflow
In this example, the workflow is triggered on a push event to the main branch. The job named ssm-parameter-update runs on the latest version of Ubuntu.

The steps within the job are as follows:

Checkout repository: This step uses the actions/checkout action to fetch the repository's code into the runner environment.

Set up AWS credentials: This step uses the aws-actions/configure-aws-credentials action to configure AWS credentials using the secrets stored in your repository settings (AWS_ACCESS_KEY_ID and AWS_SECRET_ACCESS_KEY). Replace <AWS_REGION> with the desired AWS region.

Update SSM Parameter: This step runs the aws ssm put-parameter command to update the specified SSM parameter. Replace <PARAMETER_NAME> with the name of the parameter you want to update, <NEW_PARAMETER_VALUE> with the new value for the parameter, and <PARAMETER_TYPE> with the desired parameter type (e.g., String, SecureString, StringList).

You can customize this workflow by providing your own values for the parameter name, value, and type. Additionally, you can add more steps or actions to perform additional tasks as needed.
