Lab 3 Q2 - Terraform (AWS: VPC + ALB + Auto Scaling Group)
  aws configure                # credentials
  terraform init
  terraform validate
  terraform plan -out tfplan
  terraform apply tfplan
  curl http://$(terraform output -raw alb_dns_name)
  terraform destroy            # clean up to avoid charges
