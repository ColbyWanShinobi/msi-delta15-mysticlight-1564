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


Notes/Credit:

https://gitlab.com/CalcProgrammer1/OpenRGB/-/issues/2289#note_947399598

https://weinimo.github.io/how-to-write-udev-rules-for-usb-devices.html

https://unix.stackexchange.com/questions/39370/how-to-reload-udev-rules-without-reboot

https://www.msi.com/Laptop/Delta-15-A5EX
