### Setup

This should be wrapped up into an RPM.

```
sudo dnf install sg3_utils
cp get_enclosure_slot /lib/udev/get_enclosure_slot
chmod +x /lib/udev/get_enclosure_slot
cp 60-persistent-enclosure-slot.rules /etc/udev/rules.d/
sudo udevadm trigger
```
