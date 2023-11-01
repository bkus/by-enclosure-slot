# Setup

This should be wrapped up into an RPM.

```
sudo su -
dnf -y install sg3_utils
cp get_enclosure_slot /lib/udev/get_enclosure_slot
chmod +x /lib/udev/get_enclosure_slot
cp 60-persistent-enclosure-slot.rules /etc/udev/rules.d/
udevadm trigger
```

You can now find your disks indexed by their enclosure model, address and slot within each enclosure, in `/dev/disk/by-enclosure-slot/`.

Editing the get_enclosure_slot file will allow you to alias your enclosures to what you call them.

If you look at 60-persistent-enclosure-slot.rules you can see examples on how to add NVME ports and SATA ports 
