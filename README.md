# miZy-tools

![miZy - tools](pics/mizy_tools.gif)

mizy tools collection

+ tools/`fel_full_boot`	- boot via FEL mode 
+ tools/`hybrid`	- mizy image army knife 
+ tools/`mizy_up`	- setup usb otg network to device, without dhcp
+ tools/`mizy_shell`	- ssh automate script
+ tools/`serial`	- automate serial UART console access
+ tools/.*		- just for me git usage

# install miZy-tools

mkdir /tmp/mizy_examples
cd /tmp/mizy_examples
git clone https://github.com/hyphop/miZy-tools
./prepare

# simple examples #1

boot any mizy images without write it to storage sd/mmc/spi just via usb FEL mode
yeah!!! its cool, quick and very easy!

```
# extract any downloaded mizy image

cd bin
../tools/hybrid *.bin extract
cd ..

# fel boot this image

tools/fel_full_boot

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
+ if u have any bootable source u can write by zero first 8192 bytes
+ sunxi-fel source https://github.com/hyphop/sunxi-tools

