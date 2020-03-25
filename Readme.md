rtl8821cu
( idVendor=0bda, idProduct=c811 )
driver v5.4.1_28754.20180921_COEX20180712-3232

origin : https://github.com/brektrou/rtl8821CU

Currently (march 2020) used by me on Xunlong Orange OPi H3 and H5 with Linux 5.6, Debian 10. Works great both in access point mode and in infrastructure mode.

This driver must be built in "in-tree" mode.
1. put driver sources to ".../drivers/net/wireless/realtek/rtl8821cu"
2. into file ".../drivers/net/wireless/realtek/Kconfig" insert line: 
source "/drivers/net/wireless/realtek/rtl8821cu/Kconfig"
3. into file ".../drivers/net/wireless/realtek/Makefile" insert line: 
obj-$(CONFIG_RTL8821CU) += rtl8821cu/
4. do : make menuconfig -> device drivers-> network device support -> wireless LAN -> select 8821cu
5. do make.
