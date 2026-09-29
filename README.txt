Lab 3 Q1 - Ansible
Run from the control node:
  ansible all -m ping
  ansible-playbook site.yml --syntax-check
  ansible-playbook site.yml --check      # dry run
  ansible-playbook site.yml              # apply
  ansible-playbook site.yml              # rerun -> changed=0 (idempotent)
  curl http://<node-ip>
Needs: ansible-galaxy collection install community.general





Lab 3 Q2 - Terraform (AWS: VPC + ALB + Auto Scaling Group)
  aws configure                # credentials
  terraform init
  terraform validate
  terraform plan -out tfplan
  terraform apply tfplan
  curl http://$(terraform output -raw alb_dns_name)
  terraform destroy            # clean up to avoid charges
