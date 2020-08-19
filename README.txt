# ansible-pull-example
ansible-pull-example/
├── README.md
├── ansible_test_app
│   └── ansible_app.sh
├── hosts
└── local.yml

Steps to automate
-----------------
Automate the call
		e.g. 
			Add it to your crontab.
				0 3 * * * /usr/local/bin/ansible-pull -U https://github.com/vincesesto/ansible-pull-example -i hosts
			or
         Put it in jenkins
		Add the <hostname>.yml or local.yml file to your repository.
         ansible-pull follows convention. Looks only for local.yml and <hostname>.yml
	No third step.
Cronjob to be created.
0 3 * * * /usr/local/bin/ansible-pull -U https://github.com/vilasvarghese/ansible-pull-example -i hosts

Note that ansible-pull follows conventions.

hosts, 
├──Same/similar to ansible hosts file.
├──As mentioned in the -i option.
local.yml file
├──Alternative: groupname.yml. 
├──Resides in the root of the project directory 
├──ansible-pull command looks for this file. 
├──a playbook with specific naming convention
   ├──all playbook commands and rules are applicable here as well.
├──Execution is also same as playbook.
