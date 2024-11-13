# nvidia-wayland-settings

Create a config file called nvidia.conf on:
```shell
/etc/modprobe.d/nvidia.conf
```
by typing
```shell
sudo nano /etc/modprobe.d/nvidia.conf
```

i recommend  adding this lines

```shell
#be sure to add "options" before each line
options nvidia_drm modeset=1
options nvidia_drm fbdev=1
options nvidia NVreg_EnableGpuFirmware=0
options nvidia Nvreg_PreserveVideoMemoryAllocations=1
```
Save and Then run 
```shell
sudo mkinitcpio -P
```
Reboot
