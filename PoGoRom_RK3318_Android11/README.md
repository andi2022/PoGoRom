
# PoGoRom RK3318 Chipset Android 11

**Use this rom at your own risk**

`Tested on H96Max 4GB/32GB and 4GB/64GB`

[Download beta ROM v1.0](https://github.com/andi2022/PoGoRom/releases/download/rk3318_a11/pogorom_rk3318_a11_beta_v1.0.img.zip)

From the first boot until the init script is finished, it takes about 10 minutes. The device will reboot twice while the init script is running.

**Features**
 - Skip setup wizard
 - Removed many pre installed apps
 - Removed bootanimation
 - Removed /system/sbin/su
 - init.d integraded
 - Added some terminal binaries curl,jq,nano,rsync
 - Added Magisk 27008 patched boot
 - Init script for basic setup (Magisk 27008, latest PIF module, SPIC)
 - Custom scripts from USB (Run all scripts in folder scripts every
   boot)
 - Added ADB enabled by default
 - Copy adb fingerprint from USB (Copy file adb_keys from folder
   adb_keys every boot)

**Important notes**
 - To pass basic and device integrity, the play store need updates, this
   can take a while until it's completed after the init script is
   finished.
 - USB thumb drive need to be on the BLUE USB port, closer to the reset button.
 - Log for init process is here: `/data/local/tmp/init/initrom.log`

Example USB thumb drive structure
```
USB_ROOT
	Folder
		Files

USB_ROOT
	adb_keys
		adb_keys
	scripts
		script1.sh
		script2.sh
```

**scrcpy commandline**
To connect via scrcpy, this command is working. Tested with scrcpy 2.7.
`scrcpy.exe -b2M -m1024 --video-encoder c2.android.avc.encoder --tcpip=<DeviceIP>`