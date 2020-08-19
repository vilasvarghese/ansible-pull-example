# ansible-pull-example
ansible-pull-example/
├── README.md
├── ansible_test_app
│   └── ansible_app.sh
├── hosts
└── local.yml

Cronjob to be created.
0 3 * * * /usr/local/bin/ansible-pull -U https://github.com/vilasvarghese/ansible-pull-example -i hosts

hosts, 
├──Same/similar to ansible hosts file.
├──This should be in the github/url root directory
local.yml file
├──Alternative: groupname.yml. 
├──Resides in the root of the project directory 
├──ansible-pull command looks for this file. 
├──a playbook with specific naming convention
   ├──all playbook commands and rules are applicable here as well.
├──Execution is also same as playbook.
