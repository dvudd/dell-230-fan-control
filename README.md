# dell-230-fan-control
Python script to control the fan speed on a Dell Poweredge 230

The script only works on Linux since it reads the CPU temp from /sys/class/thermal/thermal_zone1/temp

Dependencies:
[Python 3](https://www.python.org/)
[IPMItool](https://github.com/ipmitool/ipmitool)

It might work on other Dell models, the IPMItools raw data number comes from: **LINK COMING SOON**
Use at your own risk!

I run the script with systemd using the user "fan"
I've added this line to /etc/sudoers 
`fan ALL=(root) NOPASSWD: /bin/ipmitool`
