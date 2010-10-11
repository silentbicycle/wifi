This is a short script for managing auth info for multiple wireless networks on OpenBSD.

## Usage ##

Create a file, ~/.wifidat , that looks something like this:

    device="ral0"   -- device ID, as listed by ifconfig
    sudo=true       -- use sudo before ifconfig command

    Network{ key="home", nwid="thebatcave", wpa="pajamatime" }
    Network{ key="coffeeshop", nwid="Coffee Mart", wep="0xdeadbeef" }
    Network{ key="office", nwid="Corporate Guest Network", 
             wpa="meetingsFTW" }
    Network{ key="library", nwid="lib_public" }

Each Network{} definition can have the following keys:

  + key = "name"
  + nwid = "NWID"
  + wpa = WPA key
  + wep = WEP key (yeah...)

