# myFirstAnsibleProject
This is my first Ansible Project

Run below command to execute yaml file: 

ansible-playbook -i myinventoryfile myansiblefile.yaml

# Dry Run In Ansible
Ansible Dry Run or Ansible Check mode feature is to validate your playbook before execution. 
With the Ansible Dry Run feature, you can execute the playbook without having to actually make changes on the server. 
this enables us to see what changes are going to be made when the playbook is run.
### How To Dry Run An Ansible Playbook
- using check mode
  Check mode is just a simulation. It will not generate output for tasks that use conditionals based on registered variables (results of prior tasks). However, it is great for validating configuration management playbooks that run on one node at a time. To run a playbook in check mode:
### ansible-playbook main.yml --check
- using diff mode
  The --diff option for ansible-playbook can be used alone or with --check. When you run in diff mode, any module that supports diff mode reports the changes made or, if used with --check, the changes that would have been made. Diff mode is most common in modules that manipulate files (for example, the template module) but other modules might also show ‘before and after’ information (for example, the user module).

Diff mode produces a large amount of output, so it is best used when checking a single host at a time. For example:

### ansible-playbook main.yml --check --diff --limit main.example.com
  
