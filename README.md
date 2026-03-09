Role Name =========
create-host-entries

Create host entries for /etc/hosts file

Requirements
------------
Works with RHEL versions 7 - 9.  Also with FreeBSD versions 13 - 15.

Role Variables
--------------

# setup variable to hold host entriees
create_host_entries_host_file_host_entrries:
  - '10.0.0.<address> <hostname>'

Dependencies
------------
None

Example Playbook
----------------


- hosts: node4.example.com

  vars:

    create_host_entries_host_file_host_entries:
      - '10.0.0.20 node20.example.com'
      - '10.0.0.21 node21.example.com'

  roles:

    - name: create-host-entries
