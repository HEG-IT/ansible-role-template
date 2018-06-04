# ansible-role-template
Best Practices Template for use in Ansible Roles

# Sources
* http://docs.ansible.com/ansible/latest/user_guide/playbooks_best_practices.html#directory-layout
* http://docs.ansible.com/ansible/latest/user_guide/playbooks_reuse_roles.html

# Folder Structure
```
tasks/           #
   main.yml      #  <-- tasks file can include smaller files if warranted
handlers/        #
   main.yml      #  <-- handlers file   
templates/       #  <-- files for use with the template resource
   config.j2     #  <------- templates end in .j2   
files/           #
   bar.txt       #  <-- files for use with the copy resource
   foo.sh        #  <-- script files for use with the script resource   
vars/            #
    main.yml     #  <-- variables associated with this role
defaults/        #
   main.yml      #  <-- default lower priority variables for this role  
meta/            #
   main.yml      #  <-- role dependencies   
library/         # roles can also include custom modules
module_utils/    # roles can also include custom module_utils
lookup_plugins/  # or other types of plugins, like lookup in this case
