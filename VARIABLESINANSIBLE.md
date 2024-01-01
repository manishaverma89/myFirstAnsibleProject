# ANSIBLE VARIABLES
       
* Define with the file directly

* Passing from external files

* Passing from host inventory

* Using group_vars or hosts_vars and so on.......

## EXAMPLE OF DEFINING VARIBALES WITHIN A FILE

![image](https://github.com/manishaverma89/myFirstAnsibleProject/assets/84954924/255e50d6-955e-4abd-85ac-7cbfab5f5e24)


## EXTRA VARIABLES IN ANSIBLE
https://www.redhat.com/sysadmin/extra-variables-ansible-playbook

## Controlling your variables from outside of Ansible roles
Ansible roles are a collection of templates, files, variables, modules, handlers, and tasks created for the purpose of simplifying the reuse of Ansible code.

Within an Ansible role directory structure, you'll have two types of variables inside the following directories:

defaults/main.yml - contains variables for a role that can be customized based on the desired usage of the role.
vars/main.yml - contains variables for a role that are not intended to be modified.
* Due to --extra-vars having higher precedence than vars/main.yml variables can be modified using the --extra-vars parameter. Modifiable variables should reside in defaults/main.yml

You can set the variable values by using --extra-vars.

For example, using a different port in an Apache installation like below (assuming variables are defined within the defaults/main.yml):

# ansible-playbook deploy-apache.yaml --extra-vars “apache_listen_port=8080”
If you have multiple values to pass, then try this:

# ansible-playbook deploy-apache.yaml --extra-vars “apache_listen_port=8080 apache_listen_port_ssl=443”
