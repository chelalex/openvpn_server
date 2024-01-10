openvpn_server
=========

Install and configure OBFS4 ansible role<br>
Available for Ubuntu 22.04 LTS<br>

    openvpn_server
    ├── README.md
    ├── files
    │   └── make_config.sh
    ├── tasks
    │   └── main.yml
    ├── templates
    │   ├── before.rules.j2
    │   ├── client.conf.j2
    │   ├── server.conf.j2
    │   └── ufw.j2
    └── vars
        └── main.yml

Requirements
------------

Previously you should configure PKI for certficate generation and exchange necessary certificates each other.

Role Variables
--------------

openvpn_server:<br>
&nbsp; local_address: *local option value (openvpn server config file)*<br>
&nbsp; local_easy_rsa_path: *path to easyrsa launch directory*<br>
&nbsp; config_path: *path to openvpn server config files*<br>
&nbsp; dh_param: *diffie-helman option value (openvpn server config file)*<br>
&nbsp; port: *connection port option value (openvpn server config file)*<br>
&nbsp; proto: *transport protocol option value: tcp or udp (openvpn server config file)*<br>
&nbsp; cipher_mode: *cipher-mode option value (openvpn server config file)*<br>

Example Playbook
----------------

    - hosts: server
      roles:
         - openvpn_server
