### Requirements
- Ensure you have already set up your 3 'raw' vagrant boxes as detailed in github.com/jckhmr/adlab/vagrant
- You'll need to install your Ansible Controller on a .nix computer.  I used a Kali 2019.3 machine.  You can find a great guide here from <a href="https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html" target="_blank">the good folks at Ansible</a>.  I would add that the Ansible docs site is an incredibly useful resource if you want to learn more about the topic.
- On my home lab setup, once the lab was up and running, I was glad of the fact that I had 16gb of RAM (on an i7 that is nearly 10 years old).  I also needed in the region of 70gb of space.  Yes, it sounds like a lot, but consider that you will end up with a Windows 2012 R2 Domain Controller, a Windows 2012 R2 'Member Server' (file/web/SQL Server) and a Win 10 Workstation. 

### I've got everything installed, now what?
- just run the following command and it will start to run the playbook for you.

### FYI ...
- In the event that any of the playbooks ever 'time-out', from personal experience it's because my computer had simply too many other things running.  In this case .... kill off anything unnecessary and re-run the playbook command listed above.

```ansible-playbook labsetup.yml -i environments/bsides/hosts --user=vagrant -vv```

Once everything is up and running (just watch for the on-screen feedback) you can then remote desktop into each of the machines or start whatever it is you want to do.

### Other bits and pieces
General feedback is welcome ... you can find me on <a href="https://twitter.com/jckhmr_t" target="_blank">twitter (@jckhmr_t)</a>.  I also have a (small, but developing) <a href="https://jckhmr.net" target="_blank">website</a>.  

Happy Hacking .... jckhmr
