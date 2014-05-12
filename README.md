Role Name
========

Configure rsyslog collector, relay, or host depending on `group_names`. The role will install rsyslog 7 on the collector.

Requirements
------------

rsyslog >=5.8 on relay and client hosts

Role Variables
--------------

**rsyslog_tcp_port:**  TCP port for shipping unencrypted logs (default 514)
**rsyslog_udp_port:**  UDP port for shipping unencrypted logs (default 514)
**rsyslog_tls_port:**  TCP port for shipping encrypted logs (default 6514)
**rsyslog_encrypt:**   Whethere or not to enable TLS encryption (default false)
**rsyslog_protocol:**  Transport protocol, eithe TCP or UDP (default tcp)


Dependencies
------------

rsyslog must be installed on the hosts

Example Playbook
-------------------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: syslog, rsyslog_encrypt: false, rsyslog_protocol: tcp }

License
-------

MIT

