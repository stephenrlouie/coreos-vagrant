# CoreOS Vagrant for Gemini 

## Streamlined setup

1) Install dependencies

* [VirtualBox][virtualbox] 4.3.10 or greater.
* [Vagrant][vagrant] 1.6 or greater.

2) Clone this project and get it running!

```
git clone https://github.com/stephenrlouie/coreos-vagrant.git
cd coreos-vagrant
git checkout gemini
```

3) Start up the Gemini Master

```
git clone https://github.com/stephenrlouie/PXE-Boot-VM.git
cd PXE-Boot-VM
git checkout gemini
```

4) Copy the `ansible.rsa` from the Gemini Master to this home directory

5) Startup and SSH

Only tested on the virtualbox provider

**VirtualBox Provider**

The VirtualBox provider is the default Vagrant provider. Use this if you are unsure.

```
vagrant up
vagrant ssh
```

## Get started [using CoreOS][using-coreos]

[virtualbox]: https://www.virtualbox.org/
[vagrant]: https://www.vagrantup.com/downloads.html
[using-coreos]: http://coreos.com/docs/using-coreos/

## New Box Versions

CoreOS is a rolling release distribution and versions that are out of date will automatically update.
If you want to start from the most up to date version you will need to make sure that you have the latest box file of CoreOS.
Simply remove the old box file and vagrant will download the latest one the next time you `vagrant up`.

```
vagrant box remove coreos --provider vmware_fusion
vagrant box remove coreos --provider vmware_workstation
vagrant box remove coreos --provider virtualbox
```
