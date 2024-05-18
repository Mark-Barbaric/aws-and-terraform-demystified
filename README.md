# aws-and-terraform-demystified

Repository containining source code and scripts for the Medium Article I wrote about creating a NAT Instance using terraform.

## Accessing AWS Secrets via cli

### Listing all secrets

>`aws secretsmanager list-secrets`

### Get String Value from Secret

>`aws secretsmanager get-secret-value --secret-id example_ssh_key_pem_testing --query SecretString --output text`

### Using ipes to decode pem to pem format

>`aws secretsmanager get-secret-value --secret-id example_ssh_key_pem_testing --query SecretString --output text | base64 --decode > test.pem`