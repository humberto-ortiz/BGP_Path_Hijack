# BGP_path_hijack
This is demo code for the BGP Hijacking lab from the mininet repository:
<https://github.com/mininet/mininet/wiki/BGP-Path-Hijacking-Attack-Demo>

This version is modified for running on ubuntu 22.04 by Humberto Ortiz-Zuazaga, it was first ported to mininet 2.3.0 by `spwpun`:
<https://github.com/spwpun/BGP_Path_Hijack>.

This repo is different from the `https://bitbucket.org/jvimal/bgp/src`, it is an upgradable version for `Mininet 2.3.0`, check it out!
## Envs

Install the following packages with apt:

- mininet 2.3.0
- frr
- python3-termcolor
- openvswitch-testcontroller

## Steps

Follow the steps in the [mininet wiki](https://github.com/mininet/mininet/wiki/BGP-Path-Hijacking-Attack-Demo). You can skip Step 1, parts 1, 2, and 3. this repository replaces the virtual machine image and scripts described there.

In brief:
```
mininet@mininet-vm:$ git clone https://github.com/humberto-ortiz/BGP_Path_Hijack.git
mininet@mininet-vm:$ cd BGP_Path_Hijack/
mininet@mininet-vm:$ sudo python3 bgp.py
# new termial window, connect to S1 router, passwd is "en", type twice with [enter]
mininet@mininet-vm:$ ./connect.sh
bgpd-S1# show bgp all
# new another window, test web service
mininet@mininet-vm:$ ./website.sh
# new another window, start roguing AS
mininet@mininet-vm:$ ./start_rogue.sh
# check the output in `website.sh` windows
mininet@mininet-vm:$ ./stop_rogue.sh
```
