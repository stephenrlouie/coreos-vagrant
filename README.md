# CoreOS Vagrant for Gemini 
- The **Vagrant Boot Managed Nodes** for the Gemini Project.
- Must be stood up after the [Gemini Master] (https://github.com/stephenrlouie/PXE-Boot-VM/tree/gemini) is stood up so the ansibla.rsa key is present.

##Demo
- [Streaming Link] (https://cisco.webex.com/ciscosales/ldr.php?RCID=1685081ad9ff3361b1fcc68ceb24a282)
- [Download Link] (https://cisco.webex.com/ciscosales/lsr.php?RCID=b3fc3aa5faa81d5b5c608cf7199521f9)

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

3) Start up the Gemini Master. See instructions [here] (https://github.com/stephenrlouie/PXE-Boot-VM/tree/gemini)

```
git clone https://github.com/stephenrlouie/PXE-Boot-VM.git
cd PXE-Boot-VM
git checkout gemini
```

4) Copy the `ansible.rsa` from the Gemini Master to this home directory

```
cp <path_to_Gemini_Master>/ansible.rsa <path_to_coreos-vagrant>
```

5) Startup and SSH

```
vagrant up
vagrant ssh core-<number>
```

- Configure how many machines and what CoreOS image to use in the [Vagrantfile] (https://github.com/stephenrlouie/coreos-vagrant/blob/gemini/Vagrantfile)

**_Only tested on the virtualbox provider_**

##Issues
 - See the [open issues] (https://github.com/stephenrlouie/coreos-vagrant/issues) for any work-arounds needed to create the Vagrant Boot Managed Nodes
