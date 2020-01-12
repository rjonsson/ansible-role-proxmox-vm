# ansible-role-proxmox-vm
Ansible role to create a VM on Proxmox

Usage:

```

example_playbook.yml
...
- hosts: <hostname>
  remote_user: root

  roles:
    - role: proxmox-vm
      proxmox:
        api_user: "test_user@pam"
        api_password: "HardToGuessPassword"
        api_host: "ProxmoxHost"
      vm_dict:
        test_vm01:
          node: test_node
          memory: 1024
        test_vm02:
          node: test_node
          cores: 4
          memory: 4096
...
