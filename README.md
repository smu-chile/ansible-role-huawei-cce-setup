Huawei CCE Setup
=========

Ansible role to setup a bastion server to connect with a cce cluster


Role Variables
--------------

```
      KUBECONFIG: Configuration file ~/.kube/config
```

Example Playbook
----------------

```
- hosts: all
  become: no
  remote_user: "root"

  roles:
    - role: ansible-role-huawei-cce-setup
      KUBECONFIG: "{{ lookup('env', 'KUBECONFIG') }}"

```

Author Information
------------------

- [César vergara](mailto:cvergarae@smu.cl)

