Ansible Role: Semaphore
=========

An Ansible role for deploying Semaphore as a Podman container managed by systemd.

Requirements
------------

None.

Role Variables
--------------

```yaml
semaphore_podman_name: semaphore
semaphore_podman_user: semaphore
semaphore_podman_group: "{{ semaphore_podman_user }}"
semaphore_podman_network: semaphore
semaphore_podman_version: latest
semaphore_podman_db_version: latest
semaphore_podman_home: /home/semaphore
semaphore_podman_mariadb_root_passwd: changeme
semaphore_podman_db_passwd: changeme
```

Dependencies
------------

None.

Example Playbook
----------------

```yaml
- name: Deploy Semaphore
  hosts: servers
  roles:
    - role: semaphore_podman
      semaphore_podman_home: /home/semaphore
      semaphore_podman_mariadb_root_passwd: "{{ semaphore_password }}"
      semaphore_podman_db_passwd: "{{ semaphore_password }}"
```

License
-------

MIT

Author Information
------------------

This role was created by [Adam Haydon](https://github.com/ahaydon)
