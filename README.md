# dell-230-fan-control
Python script to control the fan speed on a Dell Poweredge R230

The script only works on Linux since it reads the CPU temp from '/sys/class/thermal/thermal_zone1/temp'

Dependencies:<br />
[Python 3](https://www.python.org/)<br />
[IPMItool](https://github.com/ipmitool/ipmitool)<br />

It might work on other Dell models, the IPMItools raw data number comes from: [ServerFault](https://serverfault.com/questions/1025601/control-or-reduce-fan-speed-of-dell-r820)<br />
Use at your own risk!

I run the script with systemd using the user "fan"<br />
I've added this line to /etc/sudoers <br />
`fan ALL=(root) NOPASSWD: /bin/ipmitool`
