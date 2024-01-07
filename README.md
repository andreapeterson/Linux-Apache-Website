# Linux-Apache-Website
Automatic Vagrant Provisioning- IaC to host my website via sync directory. Piggy-backing off my Cloud Resume Challenge where I hosted my portfolio website in AWS fully severless, today I decided to do the opposite- host my website on my own server! This Vagrantfile sets up a web server with Apache2 and hosts my portfolio website on it, all automatic during provisoning.

Originally, I set everything up manually first. I used the scp command to securely copy files from my local machine to the VM. However, while setting up the automation on the Vagrantfile, I decided to incorpoarte the use of sync directories (specifically rsync as the synced folder type), so the 'my_website' file on my local machine is synced to the /var/www/html/ directory in the VM, and any changes are applied on 'vagrant rsync', as seen below.

![website_iac](https://github.com/andreapeterson/Linux-Apache-Website/assets/134665743/a4956d33-1a2e-4318-a8fc-34b9a91939ea)
