# NetAidKit

Standalone VPN/Tor router for journalists and activists.

## Flashing the GL-iNet:

*   While pressing the reset button on the side of the GL-iNet,
    power on the device. You will see the green LED flashing.
    Hold the reset button until the green LED flashes 5 times.
    When the red light flashes once, release your finger.
    The device is now booting into failsafe mode.

*   Connect to the device using an ethernet cable and manually 
    set your IP address to 192.168.1.2.

*   Visit 192.168.1.1 in your browser and upload the `.bin` file 
    from the [bin](bin) folder 
    to the page and click 'Update firmware'. Wait for the device to
    reboot into the new firmware and do not turn it off.

Set-up
----
Connect to the NETAIDKIT access point using password 'netaidkit'. Browse to 192.168.101.1 and follow the steps to set-up your own AP and change the passwords.


Disconnect from wifi
----
To disconnect from a wifi network, press the reset button on the side of the device once (do not hold, simply press)


## Building the firmware image

*Pre-built binaries are available in the [bin](bin) folder.  If you want to build your own manually, instructions follow.*

Install dependencies

```bash
sudo apt-get update
sudo apt-get install git-core build-essential libssl-dev libncurses5-dev unzip subversion gawk python python-passlib jq
```


Create a working directory somewhere and execute the following commands:

```bash
git clone https://github.com/radicallyopensecurity/netaidkit
cd netaidkit && ./build.sh
```

The compiled images will be in the netaidkit/bin folder.

