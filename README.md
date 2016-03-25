# CoreOS Vagrant for Gemini 
- The **Vagrant Boot Managed Nodes** for the Gemini Project.
- Must be stood up after the [Gemini Master] (https://github.com/stephenrlouie/PXE-Boot-VM/tree/gemini) is stood up so the ansibla.rsa key is present.

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

```
vagrant up
vagrant ssh core-<number>
```

- Configure how many machines and what CoreOS image to use in the [Vagrantfile] (https://github.com/stephenrlouie/coreos-vagrant/blob/gemini/Vagrantfile)

**_Only tested on the virtualbox provider_**

##Issues
 - See the [open issues] (https://github.com/stephenrlouie/coreos-vagrant/issues) for any work-arounds needed to create the Vagrant Boot Managed Nodes
