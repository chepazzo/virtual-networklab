virtual-networklab
==================

Collection of scripts to get a virtual lab environment up and running.

Before you begin
================
You need to build yourself a VM.  This collection is not meant to provide that.  You will also need to obtain a valid and legal OS from your vendor.

Juniper
-------
Juniper does not officially support the olive platform.  The would prefer that you use their [Junosphere](http://junosphere.net) product.  Junosphere is actually quite nice and has lots of bells and whistles.  FWIW, I am also not attempting to replicate Junosphere (to be fair, I had my virtual olive ecosystem running years before Junosphere was launched).

I built my Juniper Olive via the instructions on this site:
[http://blog.gns3.net/2009/10/olive-juniper/](http://blog.gns3.net/2009/10/olive-juniper/)

Arista
------
Arista officially supports what they call vEOS.  You may obtain a copy of this from your friendly neighborhood representative.  I will attempt to include anything that is relevant to getting it up and running in this environment.

I have not had a lot of luck booting Arista from newer aboot images, so I use `Aboot-veos-serial-2.0.8.iso` for all of my VMs.

Dependencies
============

Access
------
**root** or sudo access to the box.  You will need this to be able to create the bridge and tap interfaces.  If I find a way to do this without being root, then I will modify this.

Packages
--------
I'm hoping for this to be an exhaustive list.  Here are the names of the packages in Ubuntu and LinuxMint.  They should be the same or at least similar on your OS (except Windows.  If you use Windows, you are on your own).

* uml-utilities
* bridge-utils
* qemu-kvm

Hypervisor
----------
I am focasing on QEMU-KVM.  I might get around to putting something together for VMWare or XEN or something else, or someone else is welcome to contribute.

For a headless system, I chose [Proxmox](http://www.proxmox.com) because it used KVM and had a robust web-based GUI.  There are, however, some issues getting the Olives to be able to be managed through the Proxmox web interface which I have detailed [elsewhere](http://forum.proxmox.com/archive/index.php/t-10446.html).

Bios
----
For JunOS to run in kvm, you need to use an older bios (0.10.6) which can be found here:
[http://downloads.sourceforge.net/project/kvm/qemu-kvm/0.10.6/qemu-kvm-0.10.6.tar.gz](http://downloads.sourceforge.net/project/kvm/qemu-kvm/0.10.6/qemu-kvm-0.10.6.tar.gz)
Just untar and grab the file from ./qemu-kvm-0.10.6/pc-bios/bios.bin and copy it somewhere you can access (/usr/share/qemu-kvm/bios-0.10.6.bin is probably good).
