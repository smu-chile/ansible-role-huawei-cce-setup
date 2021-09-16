Role Name
=========

Role to setup a bastion to connect with a cce cluster



Role Variables
--------------

```
KUBECONFIG
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

License
-------

BSD

Author Information
------------------

- [César vergara](mailto:cvergarae@smu.cl)