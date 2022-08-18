Ansible Role: RHEL Subscription Registration and Attachment with Activation Key
=========

Register RHEL system and attach to a subscription with Activation Key.

Requirements
------------

community.general.redhat_subscription module.

Role Variables
--------------

Available variables are listed below, along with default values (see defaults/main.yml):

```yaml
rhel_org_id: 1234567
rhel_activationkey: my_rhel_activation_key
```

Set these variables in group_vars/redhat.yml to overwrite the default value.

Dependencies
------------

None.

Example Playbook
----------------

```yaml
- hosts: servers

  tasks:
    - name: config rhel subscription
      include_role:
        name: sfitpro.rhel_subscription
        apply:
          tags:
            - rhel
      when: ansible_distribution == "RedHat"
      tags:
        - rhel
```

License
-------

BSD

Author Information
------------------

This role was created by Eddie Lu.
