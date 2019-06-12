# miZy-tools

![miZy - tools](pics/mizy_tools.gif)

mizy tools collection

+ tools/`fel_boot`	- boot via FEL mode 
+ tools/`fel_spi_info`	- boot via FEL mode 
+ tools/`fel_spi_write`	- boot via FEL mode 
+ tools/`hybrid`	- mizy image army knife 
+ tools/`mizy_up`	- setup usb otg network to device, without dhcp
+ tools/`mizy_shell`	- ssh automate script
+ tools/`mizy_ssh_image_write`	- write image via ssh
+ tools/`image_write_sd`	- write mizy image to SD card storage
+ tools/`image_write_spi`	- write mizy image to SPI flash storage
+ tools/`serial`	- automate serial UART console access
+ tools/.*		- just for me git usage

# install miZy-tools

```
mkdir /tmp/mizy_examples
cd /tmp/mizy_examples
git clone https://github.com/hyphop/miZy-tools
./prepare
```
# simple examples #1

boot any mizy images without write it to storage sd/mmc/spi just via usb FEL mode
yeah!!! its cool, quick and very easy!

```
# extract any downloaded mizy image

cd tmp
wget IMAGE
cd ..

# boot this image via FEL mode (without storage write)

tools/fel_full_boot tmp/mizy_image

# setup usb network ( if not dhcp auto configured by system )

tools/mizy_up

# ssh login to device

tools/mizy_shell

# ok!

```

# FEL mode

FEL mode activation

+ started automatically if not have any other bootable source
+ on active mizy `fel_boot_write yes` - setup FEL boot from sd
+ if u have any bootable source u can write it by zero first 8192 bytes, or just remove it
+ sunxi-fel source https://github.com/hyphop/sunxi-tools


# About miZy

miZy - tiny & fast embedded linux OS + firmware framework builder fully open-source, extreme small and stable. Optimized for H2 H3 Allwinner ARM SoCs devices, oriented for embedded, IoT, DIY, homelet devices, gadgets, and other usage.

read more about miZy there https://hyphop.github.io/mizy/

# LINKS

+ https://github.com/hyphop/miZy
+ https://github.com/hyphop/miZy-uboot
+ https://github.com/hyphop/miZy-linux-kernel
+ https://github.com/hyphop/miZy-spi-image-builder
+ https://github.com/hyphop/miZy-openwrt-sdk
+ https://github.com/hyphop/miZy-builder
+ https://github.com/hyphop/miZy-tools
+ https://github.com/hyphop/miZy-images-collection
+ https://github.com/hyphop/miZy-busybox

