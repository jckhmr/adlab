## Introducing the Active Directory Learning Lab

I'm a big fan of automation with tools such as Ansible, Vagrant and Terrorm now being put to regular use by me.  Also, as a Red Team Operator I spend a lot of time modelling attacks up, trying new ideas out and generally keeping myself 'sharp'.  I wanted to create something that help me to scratch all of this itches. The research and development culminated in my BSides Belfast 2019 presentation: <a href="https://github.com/jckhmr/presentations/blob/master/BSidesBelfast2019_Final_Optimized.pptx?raw=true" target="_blank">Offensive Ansible for Red Teams (Attack, Build, Learn)</a>.  

Even though I call this a 'learning lab', the 'learning' isn't in the setting up/configuration of the network, moreso on what you can do with a fully functioning Active Directory environment, if you are into all things Red Team / offensive security.  You want to get on with the business of learning/sharpening your offensive skillsets as opposed to spending countless hours setting the environment up.

Using the code in this repo, you will use Vagrant to create the raw basic boxes (VirtualBox) and Ansible to configure it all into to three fully functioning pieces of complete (albeit small) Active Directory environment:

- Windows 2012 R2 Domain Controller
- Windows 2012 R2 'Member Server' comprising of a file server, web server, MS SQL Server (developer edition) and MS SQL Server Management Studio
- Windows 10 Workstation

### Tear down and destroy
While the Windows machines are based upon trial versions, this doesn't mean the whole lab will only last a set period of time (e.g. 180 days for the server OS).  You can issue a 'vagrant destroy' command (in the folder where 'Vagrantfile' exists) followed by by 'vagrant up', run the Ansible playbook again, and you'll be in business.  

Keep in mind though that since you are creating the lab environment on a local computer, there is a lot of machine time - i.e. downloading stuff.  Be patient per the horsepower available to you (local machine and Internet connection).  Just by way of example, the total time to build and configure the boxes was around 2 hours for me.  

### Some advice
- Create some regular snapshots, just in case anything goes south when you are conducting your hacking/security research
- Do not expose the lab to the Internet or rely upon it for production purposes.  None of the machines are 'hardened' in any way, so caution is advised.
- I've primarily tested this on a Kali 2019.3 machine

### Kudos to the community
I spent a LOT of timing researching this stuff and inevitably I came across lots of useful information out there online.  One source in particular is <a href="https://github.com/kkolk" target="_blank">kkolk</a> - their Microsoft SQL Server Ansible role is included here with perhaps a few very minor modifications/additions. Thanks kkolk! 

### Next Steps
General feedback is welcome ... you can find me on <a href="https://twitter.com/jckhmr_t" target="_blank">twitter (@jckhmr_t)</a>. I also have a (small, but developing) <a href="https://jckhmr.net" target="_blank">website</a>.  

Happy Hacking .... jckhmr 
