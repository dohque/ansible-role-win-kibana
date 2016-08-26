Ansible Role: win_kibana
========================

[![Build Status](https://travis-ci.org/dohque/ansible-role-win-kibana.svg?branch=release)](https://travis-ci.org/dohque/ansible-role-win-kibana)

An Ansible Role that installs Kibana on Windows.


Requirements
------------

Windows box should be prepared and configured to be accessible by Ansible.

<http://docs.ansible.com/ansible/intro_windows.html#windows-system-prep>


Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

```yaml
kibana_version: 4.5.4
```

Version of Kibana to be installed.

```yaml
kibana_server_host: "localhost"
```

Network host to listen for incoming connections on. By default we only listen
 on the localhost interface. Change this to the IP address to listen on a
 specific interface, or 0.0.0.0 to listen on all interfaces.

```yaml
kibana_server_port: 5601
```

The port to listen for HTTP connections on.

```yaml
kibana_elasticsearch_url: "http://localhost:9200"
```

Elasticsearch hosts Kibana will connect to.

Dependencies
------------

  None.

Example Playbook
----------------

```yaml
    - hosts: servers
      roles:
         - { role: dohque.win_kibana }
```

Contributions
-------------

I will really appreciate any feedback and contributions. Feel free to contact me.

License
-------

MIT

Author Information
------------------

This role was created in 2016 by Ruslan Pilin.
