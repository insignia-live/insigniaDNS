### This server will allow you to connect to Insignia when your Internet Service Provider does not work with custom DNS.

## Setup

The setup process does not differ from what is shown at https://insignia.live/connect except for the values to enter in your custom DNS settings.

First, make sure that your console is connected to the same network as this computer.

Please submit any issues either via our [Discord server](https://insig.uk/discord), or [Insignia support](https://support.insignia.live).

## Running on Windows:

Run the .exe provided in this release. You may have to click past a warning from Windows SmartScreen (as it sometimes turns its nose up at applications bundled by Nuitka) or your firewall (as it needs to listen for DNS requests).

## Running on anything else:

Required packages are installable with the following command:

    sudo python3 -m pip install -r requirements.txt

Required Python version: 3.6+, tested with 3.9.9

    sudo python3 insigniaDNS.py

Note: `python3` is assumed to be the name of your python binary, if it is not then it will need to be substituted with the name and/or path of your binary.

## What you'll see when it starts up

	+===============================+
	|      Insignia DNS Server      |
	|         Version 1.0         |
	+===============================+

	== Welcome to insigniaDNS! ==
	This server will allow you to connect to Insignia when your Internet Service Provider does not work with custom DNS.

	== How To Use ==
	First, make sure that your console is connected to the same network as this computer.

	Then, put these settings in for DNS on your console:
	~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
	Primary DNS:   XXX.XXX.XXX.XXX (NOTE: This value will be unique when you run the program)
	Secondary DNS: 001.001.001.001
	~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

	== Getting Help ==
	Need help? Visit our Discord server or check out https://support.insignia.live

## Building on Windows

- Install Python 3.6+ (preferably 3.9). Make sure to install the x86 version for 32 bit targets. 

- Install all requirements via the following command as an administrator

```
python -m pip install -r requirements.txt nuitka zstandard
```

- Run the following (answer yes to any prompts):

```shell
python -m nuitka --standalone --onefile --windows-icon-from-ico=insigniaDNS_icon.ico -o insigniaDNS.exe insigniaDNS.py
```

- Run `insigniaDNS.exe`

## Credits

Original code created by the Sudomemo Team - https://github.com/Sudomemo/sudomemoDNS