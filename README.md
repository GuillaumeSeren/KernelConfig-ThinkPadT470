KernelConfig-ThinkPadX260
==========================
My Linux Kernel configuration for a Lenovo ThinkPad X260

## Minimal but I still need:
* btrfs
* luks
* systemd
* qemu
* docker
* The gcc  optimisations [patch](https://github.com/graysky2/kernel_gcc_patch) for Intel Skylake
* Gentoo [experimental patches](https://wiki.gentoo.org/wiki/Project:Kernel/Experimental)
* The dm-crypt [options](https://wiki.gentoo.org/wiki/Dm-crypt)

## My 'lspci -nnk':
```
00:00.0 Host bridge [0600]: Intel Corporation Xeon E3-1200 v6/7th Gen Core Processor Host Bridge/DRAM Registers [8086:5904] (rev 02)
        Subsystem: Lenovo Xeon E3-1200 v6/7th Gen Core Processor Host Bridge/DRAM Registers [17aa:2245]
00:02.0 VGA compatible controller [0300]: Intel Corporation HD Graphics 620 [8086:5916] (rev 02)
        Subsystem: Lenovo HD Graphics 620 [17aa:2245]
        Kernel driver in use: i915
00:14.0 USB controller [0c03]: Intel Corporation Sunrise Point-LP USB 3.0 xHCI Controller [8086:9d2f] (rev 21)
        Subsystem: Lenovo Sunrise Point-LP USB 3.0 xHCI Controller [17aa:2245]
        Kernel driver in use: xhci_hcd
00:14.2 Signal processing controller [1180]: Intel Corporation Sunrise Point-LP Thermal subsystem [8086:9d31] (rev 21)
        Subsystem: Lenovo Sunrise Point-LP Thermal subsystem [17aa:2245]
00:15.0 Signal processing controller [1180]: Intel Corporation Sunrise Point-LP Serial IO I2C Controller #0 [8086:9d60] (rev 21)
        Subsystem: Lenovo Sunrise Point-LP Serial IO I2C Controller [17aa:2245]
00:16.0 Communication controller [0780]: Intel Corporation Sunrise Point-LP CSME HECI #1 [8086:9d3a] (rev 21)
        Subsystem: Lenovo Sunrise Point-LP CSME HECI [17aa:2245]
00:1c.0 PCI bridge [0604]: Intel Corporation Sunrise Point-LP PCI Express Root Port #1 [8086:9d10] (rev f1)
        Kernel driver in use: pcieport
00:1c.6 PCI bridge [0604]: Intel Corporation Sunrise Point-LP PCI Express Root Port #7 [8086:9d16] (rev f1)
        Kernel driver in use: pcieport
00:1d.0 PCI bridge [0604]: Intel Corporation Sunrise Point-LP PCI Express Root Port #9 [8086:9d18] (rev f1)
        Kernel driver in use: pcieport
00:1d.2 PCI bridge [0604]: Intel Corporation Device [8086:9d1a] (rev f1)
        Kernel driver in use: pcieport
00:1f.0 ISA bridge [0601]: Intel Corporation Device [8086:9d4e] (rev 21)
        Subsystem: Lenovo Device [17aa:2245]
00:1f.2 Memory controller [0580]: Intel Corporation Sunrise Point-LP PMC [8086:9d21] (rev 21)
        Subsystem: Lenovo Sunrise Point-LP PMC [17aa:2245]
00:1f.3 Audio device [0403]: Intel Corporation Sunrise Point-LP HD Audio [8086:9d71] (rev 21)
        Subsystem: Lenovo Sunrise Point-LP HD Audio [17aa:2245]
        Kernel driver in use: snd_hda_intel
        Kernel modules: snd_hda_intel
00:1f.4 SMBus [0c05]: Intel Corporation Sunrise Point-LP SMBus [8086:9d23] (rev 21)
        Subsystem: Lenovo Sunrise Point-LP SMBus [17aa:2245]
        Kernel driver in use: i801_smbus
        Kernel modules: i2c_i801
00:1f.6 Ethernet controller [0200]: Intel Corporation Ethernet Connection (4) I219-LM [8086:15d7] (rev 21)
        Subsystem: Lenovo Ethernet Connection (4) I219-LM [17aa:2245]
        Kernel driver in use: e1000e
        Kernel modules: e1000e
04:00.0 Network controller [0280]: Intel Corporation Wireless 8265 / 8275 [8086:24fd] (rev 78)
        Subsystem: Intel Corporation Dual Band Wireless-AC 8265 [8086:0010]
        Kernel driver in use: iwlwifi
        Kernel modules: iwlwifi
3e:00.0 Non-Volatile memory controller [0108]: Samsung Electronics Co Ltd NVMe SSD Controller SM961/PM961 [144d:a804]
        Subsystem: Samsung Electronics Co Ltd NVMe SSD Controller SM961/PM961 [144d:a801]
        Kernel driver in use: nvme
```

## The 'lsusb'
```
Bus 002 Device 011: ID 0bda:0316 Realtek Semiconductor Corp.
Bus 002 Device 001: ID 1d6b:0003 Linux Foundation 3.0 root hub
Bus 001 Device 006: ID 138a:0097 Validity Sensors, Inc.
Bus 001 Device 005: ID 13d3:5619 IMC Networks
Bus 001 Device 020: ID 1199:9079 Sierra Wireless, Inc.
Bus 001 Device 002: ID 058f:9540 Alcor Micro Corp. AU9540 Smartcard Reader
Bus 001 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
```

## Links
Links form inspirations:
* Gentoo Pappy's Kernel Seeds: https://forums.gentoo.org/viewtopic-t-887894.html
* KernelHub: http://www.kernelhub.org/
* Gentoo Kernel Seeds: https://wiki.gentoo.org/wiki/Kernel/Configuration/Kernel_Seeds
* Funtoo Kernel Seeds: http://www.funtoo.org/Talk:Kernel_Seeds
