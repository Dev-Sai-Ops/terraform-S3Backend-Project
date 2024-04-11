
## Install Terraform

```bash
sudo apt-get update && sudo apt-get install -y gnupg software-properties-common
wget -O- https://apt.releases.hashicorp.com/gpg | \
gpg --dearmor | \
sudo tee /usr/share/keyrings/hashicorp-archive-keyring.gpg > /dev/null
gpg --no-default-keyring \
--keyring /usr/share/keyrings/hashicorp-archive-keyring.gpg \
--fingerprint
echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] \
https://apt.releases.hashicorp.com $(lsb_release -cs) main" | \
sudo tee /etc/apt/sources.list.d/hashicorp.list
sudo apt update
sudo apt-get install terraform -y
terraform --version
```

# Execute Steps

### for initaizing S3 Backend
```bash
terraform init
```

### for formatting terraform files
```bash
terraform fmt
```

### for validateing your code
```bash
terraform validate
```

### paln for checking which resources 
```bash
terraform plan
```

### to apply 
```bash
terraform apply --auto-approve
```

### to destroy created infrastructure
```bash
terraform destroy --auto-approve
```





