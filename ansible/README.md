## Getting Started

The Ansible playbooks and roles made available here where created as part of a talk I delivered as part of <a href="https://bsidesbelfast.org">BSidesBelfast 2019</a>.  The idea being that you can take three Vagrant boxes and turn them into a 'learning network'.  The 'learning' isn't in the setting up/configuration of the network, moreso on what you can do with a fully functioning Active Directory environment if you are into all things Red Team / offensive security.  You want to get on with the business of learning/sharpening your offensive skillsets as opposed to spending countless hours setting the environment up.

I spent a LOT of timing researching this stuff and inevitably I came across lots of useful information out there online.  One source in particular is github.com/kkolk - their Microsoft SQL Server Ansible role is included here with perhaps a few very minor modifications/additions.  

### Requirements
- Ensure you have already set up your 3 'raw' vagrant boxes as detailed in github.com/jckhmr/adlab/vagrant
- You'll need to install your Ansible Controller on a .nix computer.  I used a Kali 2019.3 machine.  You can find a great guide here from <a href="https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html" target="_blank">the good folks at Ansible</a>.  I would add that the Ansible docs site is an incredibly useful resource if you want to learn more about the topic.

### I've got everything installed, now what?
- just run the following command and it will start to run the playbook for you.

```ansible-playbook labsetup.yml -i environments/bsides/hosts --user=vagrant -vv```

kj
