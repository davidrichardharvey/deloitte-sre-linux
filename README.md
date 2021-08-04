# Deloitte SRE Linux

## Vagrant Commands

(All of these commands assume that your working directory contains a Vagrantfile)

| Command | Description |
|--------|--------|
| vagrant up | Start the virtual machine |
| vagrant halt | Shut down the virtual machine |
| vagrant suspend | Sleep the virtual machine (saves the exact machine state, but has to hold this in your machine's memory) |
| vagrant destroy | Remove the machine (any changes made will be wiped) |
| vagrant destroy -f | As above, but it won't ask if you're sure |
| vagrant ssh | Connect to the vagrant VM using secure shell |
| vagrant status | Check the status of any vagrant machines outlined in the Vagrantfile |

## Package Management

| RedHat Command | 	Debian Command| 
|----------------| ---------------| 
| `rpm -i packageName`	| `dpkg -i packageName`| 
| `rpm -e packageName`	| `dpkg -r packageName` / `dpkg --purge packageName`| 
| `rpm -qa	dpkg -l` / `rpm -ql packageName`	| `dpkg -L packageName`| 
| `yum install packageName`	| `apt-get install packageName`| 
| `yum erase packageName`	| `apt-get remove packageName` / `apt-get purge packageName` (NOTE: purge is more like the remove in RedHat)| 
| `yum search searchString`	| `apt-cache search searchString`| 
