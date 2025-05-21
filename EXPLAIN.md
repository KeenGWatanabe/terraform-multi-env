variable.tf is the key
prod.tfvars, dev.tfvars, uat.tfvars are hosting the assigned variables to use.

![tfvars to input to variables.tf](/images/prod-variablesRelation.png)

$ terraform workspace new dev
$ terraform workspace list
$ terraform workspace select dev

for powershell
$ terraform plan -var-file="dev.tfvars"

# .github/workflows/main.yaml
Add your .github/workflows/main.yml file that contains your Github Actions CI/CD steps which should include configuring AWS credentials, terraform init, terraform select workspace , terraform plan -var-file=.tfvars