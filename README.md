Ansible Role: Network setup for Raspbian
=========

Configure network settings of Raspbian.
This role performs the following tasks.

- Set WiFi SSID and psk (tags: wifi)

All the tasks need root privilege.

Requirements
------------

None.

Role Variables
--------------
Available variables are listed below.

A list of dictionary composed of ssid and plain pass phrase of wifi.

``` yaml
raspbian_network_wifi:
  - {SSID: "wifi1", PASS: "passphrase_of_wifi1"}
  - {SSID: "wifi2", PASS: "passphrase_of_wifi2"}
```

Dependencies
------------

None.

Example Playbook
----------------

``` yaml
- hosts: all
  vars_files:
    - var/wifi_key.yml
  roles:
    - { role: raspbian_network}
```

License
-------

MIT

