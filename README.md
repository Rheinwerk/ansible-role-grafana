Grafana
=========

This role installes Grafana with opiniated default settings.

[![Build Status](https://travis-ci.org/Rheinwerk/ansible-role-grafana.svg?branch=master)](https://travis-ci.org/Rheinwerk/ansible-role-grafana)

Requirements
------------

None.

Role Variables
--------------

There are two variables that drive this role: `_grafana` and `RW_APT_CACHE_UPDATE`. `_grafana` is a map that contains all configuration and settings for this role. `RW_APT_CACHE_UPDATE` may be specified as an _extra variable_ on invocation of Ansible in order to force `apt-get update`. Please see `defaults/main.yml` for details.

Dependencies
------------

None.

Example Playbook
----------------

The general contract of this role is to take the variables map `_grafana` from `defaults/main.yml` as a template for your configuration and pass that configuration as a parameter to this role.

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      var:
        GRAFANA:
          ...
      roles:
         - { role: grafana, tags: [ 'grafana' ], _grafana: "{{ GRAFANA }}" }

License
-------

Please see LICENSE.

Author Information
------------------

Original author is [Lukas Pustina](https://github.com/lukaspustina) as member of the [Rheinwerk](https://github.com/Rheinwerk) project.

