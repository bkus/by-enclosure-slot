# Setup

This should be wrapped up into an RPM.

```
sudo dnf -y install sg3_utils
sudo cp get_enclosure_slot /lib/udev/get_enclosure_slot
sudo chmod +x /lib/udev/get_enclosure_slot
sudo cp 60-persistent-enclosure-slot.rules /etc/udev/rules.d/
sudo udevadm trigger
```

You can now find your disks indexed by their enclosure model, address and slot within each enclosure, in `/dev/disk/by-enclosure-slot/`.
