Lab 3 Q1 - Ansible
Run from the control node:
  ansible all -m ping
  ansible-playbook site.yml --syntax-check
  ansible-playbook site.yml --check      # dry run
  ansible-playbook site.yml              # apply
  ansible-playbook site.yml              # rerun -> changed=0 (idempotent)
  curl http://<node-ip>
Needs: ansible-galaxy collection install community.general
