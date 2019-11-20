## Introducing the Active Directory Learning Lab

I'm a big fan of automation with tools such as Ansible, Vagrant and Terrorm.  Also, as a Red Team Operator I spend a lot of time modelling attacks up, trying new ideas out and generally keeping myself 'sharp'.  I wanted to create something that help me to scratch all of this itches. The research and development culminated in my BSides Belfast 2019 presentation: Offensive Ansible for Red Teams (Attack, Build, Learn).  

Even though I call this a 'learning lab', the 'learning' isn't in the setting up/configuration of the network, moreso on what you can do with a fully functioning Active Directory environment if you are into all things Red Team / offensive security.  You want to get on with the business of learning/sharpening your offensive skillsets as opposed to spending countless hours setting the environment up.

Using the code in this repo, you will use Vagrant to create the raw basic boxes and Ansible to configure in to three fully functioning pieces of complete (albeit small) Active Directory environment:

- Windows 2012 R2 Domain Controller
- Windows 2012 R2 'Member Server' comprising of a file server, web server, MS SQL Server (developer edition) and MS SQL Server Management Studio
- Windows 10 Workstation.

### Kudos to the community
I spent a LOT of timing researching this stuff and inevitably I came across lots of useful information out there online.  One source in particular is <a href="https://github.com/kkolk" target="_blank">kkolk</a> - their Microsoft SQL Server Ansible role is included here with perhaps a few very minor modifications/additions.  
