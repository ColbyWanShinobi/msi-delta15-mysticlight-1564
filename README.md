# msi-delta15-mysticlight-1564

Under conda, running pythoon 3.9 on Ubuntu 22.04:
* pip install hid
* sudo apt install libhidapi-hidraw0



make a file: /etc/udev/rules.d/10-local.rules

it only needs one line

SUBSYSTEMS=="usb", ATTRS{product}=="MysticLight MS-1562", GROUP:="sudo"

save it

then run:

sudo udevadm control --reload-rules && sudo udevadm trigger

then run:

sudo udevadm test /devices/pci0000:00/0000:00:08.1/0000:07:00.3/usb1/1-4

