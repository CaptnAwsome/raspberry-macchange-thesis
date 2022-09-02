# raspberry-macchange
A startup script used to change the mac address of a raspberry pi.

This startup script and the usage is based on the following articles:

(1) change ip per command: https://kalitut.com/change-raspberry-pi-mac-address/ , Accessed: 02.09.2022

(2) create bash script: https://it-learner.de/linux-bash-script-erstellen/ , Accessed: 02.09.2022

(3) Add systemd unit (=> usage): https://linuxhint.com/use-etc-rc-local-boot/ , Accessed: 02.09.2022


Usage (as seen in (3) ):

1. Place the shellscrip linuxshint.sh into /usr/sbin

2. Replace "XX:XX:XX:XX:XX:XX" in the line "ifconfig eth0 hw ether XX:XX:XX:XX:XX:XX" with the desired MAC address.

3. Put changemac.service into /etc/systemd/system

4. Run "sudo systemctl enable changemac"

5. Run "systemctl start linuxhint" to start the service and "systemctl status linuxhint" to see its status.
