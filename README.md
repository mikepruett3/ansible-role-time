Ansible Role: System Time
=========

Ansible role to configure System Time settings on Linux Servers.

Requirements
------------

The role does not require anyting to run on RHEL and its derivatives.

Role Variables
--------------

Available variables are listed below, along with default values (see ```defaults/main.yml```):

``` yaml
ntp_servers:
  - 3.pool.ntp.org prefer trust
  - 2.pool.ntp.org
timezone: "America/Chicago"
```

```ntp_servers``` **(Required)** List of NTP servers to use in the configuration file.

```timezone``` **(Required)** Timezone to use when configuring the server.

Role variables can be stored with the hosts.yaml file, or in the main variables file.

Dependencies
------------

None.

Example Playbook
----------------

``` yaml
    - hosts: servers
      roles:
         - role: mikepruett3.time
```

License
-------

MIT

Author Information
------------------

Role created by [mikepruett3](https://github.com/mikepruett3) on [Github.com](https://github.com/mikepruett3/ansible-role-time)
