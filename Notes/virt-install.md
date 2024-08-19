Setting up virt-install command line to define the Fedora VM:

Replicating Fedora40-Try0 VM
Using virt-install on SLES15.5 hypervisor

```
virt-install --name f40-test-srv1 \  
    --metadata title="Fedora 40 Test Server 1" \  
    --osinfo fedora-unknown \  
    --memory 2048 --vcpus 2 \  
    --disk /dev/bk0-virtvg/f40-test-srv1 \  
    --cdrom /var/lib/libvirt/images/Fedora-Server-dvd-x86_64-40-1.14.iso \  
    --network bridge="br0",model="virtio" \  
    --graphics type="spice",listen="127.0.0.1"
```
