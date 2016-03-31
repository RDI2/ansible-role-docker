Ansible Role - docker
=====================

This role installs Docker.

Platform
--------

CentOS 7.2 is the only platform that is supported and tested so far.

Role Variables
--------------

Check out [defaults/main.yml](defaults/main.yml)

Dependencies
------------

None.

Installation
------------

Regular installation:

```bash
ansible-galaxy install RDI2.docker
```

Install the role to a specific directory(e.g. `roles/` ):

```bash
ansible-galaxy install -p roles/ RDI2.docker
```

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
    - { role: RDI2.docker }
```

If you want to enable user namespaces, set the variable `setup_user_namespaces: true` like this:

```yaml
- hosts: servers
  vars:
    setup_user_namespaces: true
  roles:
    - { role: RDI2.docker }
```

License
-------

MIT License.

Author Information
------------------

* Koji Tanaka, RDI2
