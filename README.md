configure_systemd-resolved
=========

Configure systemd-resolved

Requirements
------------

None.

Role Variables
--------------

- `nameservers`: which nameservers to use (default: use three privacy friendly ones)
- `search_domains`: search domain(s) to add to resolv.conf (will be omitted if not set)
- `dnssec_enabled`: whether to enable DNSSEC (default: `true`)

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - role: 'johanneskastl.configure_systemd-resolved'
          vars:
            nameservers:
              - '192.168.0.1'
            search_domains:
              - 'example.org'

License
-------

BSD-3-Clause

Author Information
------------------

I am Johannes Kastl, reachable via kastl@b1-systems.de.
