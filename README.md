GENERATE SWITCH CONFIGURATIONS
=======

This playbook allows you to generate switch configurations with an Ansible Playbook.

### To Run:

From the linux shell, you will need to use the ansible-playbook command, using --extra-vars or -e to specify your switch.

You will need to specify the following variables:

- name (Switch Hostname)
- po (Port count)
- ip (IP address of switch)
- gw (Default gateway for the switch)
- BU (Business Unit, defined as BU-####)

An example looks like this:  
```
ansible-playbook create_configs.yml -e '{"name":"SW01","po":24,"ip":"1.1.1.1","gw":"2.2.2.2","BU":"BU-1234"}'
```

### Output
The generated configuration will be created in the ./configs folder.
