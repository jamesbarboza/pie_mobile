# pie_mobile

For development, install the raspbian OS.
Raspberry Pi's Image can be found [here](https://www.raspberrypi.org/software/). This will take care of installation of the OS on the SD card. If you're on Linux (not Ubuntu), take a look at the `dd` command.

## Raspberry Pi setup

For ease of development, set the default passwords to this (this is just for dev)
```bash
pi: raspberrypi
root: root
```

This will install the openssh server and make sure it starts on boot
```bash
sudo apt-get update
sudo apt-get install -y openssh-server
sudo chmod +x /etc/init.d/ssh
sudo chown root:root /etc/init.d/ssh
sudo update-rc.d ssh defaults
sudo update-rc.d ssh enable
sudo /etc/init.d/ssh start
sudo /etc/init.d/ssh status
```

## Licence
[Apache 2.0](https://github.com/jamesbarboza/pie_mobile/blob/main/LICENSE)
