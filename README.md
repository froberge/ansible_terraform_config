# ansible_terraform_config

#### Appendix

Usefull command to test the Terraform provisioning locally.

* Initialized the current working directory
    ```
        terraform init
    ```
* Get a preview of what the code will do
    ```
    terraform plan -var-file="local.tfvars"
    ```
* Apply the desired changes
    ```
    terraform apply -var-file="local.tfvars" -auto-approve
    ```
* Destroy what you just created
    ```
    terraform destroy -var-file="local.tfvars" -auto-approve
    ```



ansible-vault decrypt terraform.tfstate terraform.tfstate.backup terraform.tfvars

ansible-vault encrypt terraform.tfstate terraform.tfstate.backup terraform.tfvars


---