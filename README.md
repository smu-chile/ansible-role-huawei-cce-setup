Huawei CCE Setup
=========

Ansible role to setup a bastion server to connect with a cce cluster


Role Variables
--------------

```
      KUBECONFIG: Archivo de configuración ~/.kube/config, este archivo se obtiene de terraform
```

Example Playbook
----------------

```
- hosts: all
  become: no
  remote_user: "root"

# Uncomment "aws-eks-setup" role only if you are upgrading the cluster
  roles:
    - role: ansible-role-huawei-cce-setup
      KUBECONFIG: "{{ lookup('env', 'KUBECONFIG') }}"

```

Author Information
------------------

- [César vergara](mailto:cvergarae@smu.cl)

