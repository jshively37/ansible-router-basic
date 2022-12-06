# Basic Cisco Ansible

This repo contains basic examples of using Ansible to manage a single router with a static inventory file.

This is not designed for production but basic demo.

## Installation

A requirements.txt file has been included with the dependancies. A virtual environment is highly recommended. Future changes will incorporate a Dockerfile for Docker development.

```
pip install -r requirements.txt
```

## Running

A sample inventory can be found in the `inventory\` directory.

To run the playbooks:
`ansible-playbook -i inventory/ (filename).yml`

The following files have been included:
`gather_facts.yml`: This will connect to the router and run a show version. It uses cli_parse and ntc_templates to return structured data, and displays the device's running image.

`configure_hostname.yml`: This will connect to the device and ensure the hostname matches the hostname in the inventory.

`configure_ospf.yml`: This will connect to the device and do a basic OSPF configuration.
