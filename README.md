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

Also, I am focasing on QEMU-KVM.  I might get around to putting something together for VMWare or XEN or something else, or someone else is welcome to contribute.
