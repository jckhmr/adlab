## Getting Started

The Ansible playbooks and roles made available here where created as part of a talk I delivered as part of <a href="https://bsidesbelfast.org">BSidesBelfast 2019</a>.  The idea being that you can take three Vagrant boxes and turn them into a 'learning network'.  The 'learning' isn't in the setting up/configuration of the network, moreso on what you can do with a fully functioning Active Directory environment if you are into all things Red Team / offensive security.  You want to get on with the business of learning/sharpening your offensive skillsets as opposed to spending countless hours setting the environment up.

I spent a LOT of timing researching this stuff and inevitably I came across lots of useful information out there online.  One source in particular is <a href="https://github.com/kkolk" target="_blank">kkolk</a> - their Microsoft SQL Server Ansible role is included here with perhaps a few very minor modifications/additions.  

### Requirements
- Ensure you have already set up your 3 'raw' vagrant boxes as detailed in github.com/jckhmr/adlab/vagrant
- You'll need to install your Ansible Controller on a .nix computer.  I used a Kali 2019.3 machine.  You can find a great guide here from <a href="https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html" target="_blank">the good folks at Ansible</a>.  I would add that the Ansible docs site is an incredibly useful resource if you want to learn more about the topic.
- On my home lab setup, once the lab was up and running, I was glad of the fact that I had 16gb of RAM (on an i7 that is nearly 10 years old).  I also needed in the region of 70gb of space.  Yes, it sounds like a lot, but consider that you will end up with a Windows 2012 R2 Domain Controller, a Windows 2012 R2 'Member Server' (file/web/SQL Server) and a Win 10 Workstation. 

### I've got everything installed, now what?
- just run the following command and it will start to run the playbook for you.

```ansible-playbook labsetup.yml -i environments/bsides/hosts --user=vagrant -vv```

Once everything is up and running (just watch for the on-screen feedback) you can then remote desktop into each of the machines or start whatever it is you want to do.

### Some advice
- Create some regular snapshots, just in case anything goes south when you are conducting your hacking/security research
- Do not expose the lab to the Internet or rely upon them for production purposes.  None of the machines are 'hardened' in any way.
- I've primarily tested this on a Kali 2019.3 environment

Happy Hacking .... j
