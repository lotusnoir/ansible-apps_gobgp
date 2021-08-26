# Ansible Role: ansible-apps_gobgp

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_gobgp.svg?branch=master)](https://travis-ci.com/lotusnoir/ansible-apps_gobgp)[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen)](https://opensource.org/licenses/Apache-2.0)[![Ansible Role](https://img.shields.io/badge/ansible%20role-apps__gobgp-blue)](https://galaxy.ansible.com/lotusnoir/ansible-apps_gobgp/)[![GitHub tag](https://img.shields.io/badge/version-latest-blue)](https://github.com/lotusnoir/ansible-apps_gobgp/tags)

Deploy [gobgp](https://github.com/osrg/gobgp) .

## Role variables

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `gobgp_version` | 1.2.0 | gobgp version |
| `gobgp_temp_dir` | /tmp | temporary directory to uncompress package |
| `gobgp_install_dir` | /usr/local/bin | directory to install binary |
| `gobgp_force_install` | false | force install variable |

## Examples

	---
	- hosts: apps_gobgp
	  become: yes
	  become_method: sudo
	  gather_facts: yes
	  roles:
	    - role: ansible-apps_gobgp
	  environment: 
	    http_proxy: "{{ http_proxy }}"
	    https_proxy: "{{ https_proxy }}"
	    no_proxy: "{{ no_proxy }}

## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.
