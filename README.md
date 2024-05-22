# Ansible Collection for Semaphore

This collection includes roles to deploy Semaphore with Podman and systemd.

## Installation

The collection can be installed with `ansible-galaxy`:

```sh
ansible-galaxy collection install git+https://github.com/ahaydon/ansible-semaphore-collection.git
```

## Usage

```yaml
- role: semaphore_podman
  semaphore_podman_home: /home/semaphore
  semaphore_podman_mariadb_root_passwd: "{{ semaphore_password }}"
  semaphore_podman_db_passwd: "{{ semaphore_password }}"
```

## License

This Ansible collection is [MIT licensed](LICENSE)

