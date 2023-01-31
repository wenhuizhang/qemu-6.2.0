# QEMU





## 1. Dependencies 

1. Ninja

```
sudo wget -qO /usr/local/bin/ninja.gz https://github.com/ninja-build/ninja/releases/latest/download/ninja-linux.zip
sudo gunzip /usr/local/bin/ninja.gz
sudo chmod a+x /usr/local/bin/ninja
ninja --version
```

2. glib-2.56 gthread-2.0

```
apt-get --reinstall install libglib2.0
```

3. pixman-1

```
sudo apt-get install -y libpixman-1-dev
```


## 2. Build

```
mkdir build
cd build
../configure --enable-kvm --target-list=x86_64-softmmu
```

Change configuration 

```
make
```

Configuration
```
# Boards
CONFIG_ACPI_PCI=y
CONFIG_I440FX=y
CONFIG_ISAPC=n
CONFIG_Q35=y

# VM port
CONFIG_VMMOUSE=n
CONFIG_VMPORT=n

# VMWARE
CONFIG_VMW_PVSCSI_SCSI_PCI=n
CONFIG_VMXNET3_PCI=n

# Audio and sound cards
CONFIG_AC97=n
CONFIG_ADLIB=n
CONFIG_CS4231A=n
CONFIG_ES1370=n
CONFIG_GUS=n
CONFIG_HDA=n
CONFIG_SB16=n
CONFIG_SD=n

# Automotive
CONFIG_CAN_BUS=n
CONFIG_CAN_CTUCANFD=n
CONFIG_CAN_PCI=n
CONFIG_CAN_SJA1000=n

# Network
CONFIG_E1000_PCI=n
CONFIG_E1000E_PCI_EXPRESS=n
CONFIG_EEPRO100_PCI=n
CONFIG_NE2000_COMMON=n
CONFIG_NE2000_ISA=n
CONFIG_NE2000_PCI=n
CONFIG_PCNET_COMMON=n
CONFIG_PCNET_PCI=n
CONFIG_ROCKER=n
CONFIG_RTL8139_PCI=n

# USB
CONFIG_USB=n
CONFIG_USB_AUDIO=n
CONFIG_USB_EHCI=n
CONFIG_USB_EHCI_PCI=n
CONFIG_USB_NETWORK=n
CONFIG_USB_OHCI=n
CONFIG_USB_OHCI_PCI=n
CONFIG_USB_SERIAL=n
CONFIG_USB_SMARTCARD=n
CONFIG_USB_STORAGE_BOT=n
CONFIG_USB_STORAGE_MTP=n
CONFIG_USB_STORAGE_UAS=n
CONFIG_USB_TABLET_WACOM=n
CONFIG_USB_UHCI=n
CONFIG_USB_XHCI=n
CONFIG_USB_XHCI_NEC=n
CONFIG_USB_XHCI_PCI=n

# ISA
CONFIG_IDE_ISA=n
CONFIG_ISA_DEBUG=n
CONFIG_ISA_IPMI_BT=n
CONFIG_ISA_IPMI_KCS=n

# VGA
CONFIG_ATI_VGA=n
CONFIG_VGA=n
CONFIG_VGA_CIRRUS=n
CONFIG_VGA_ISA=n
CONFIG_VGA_PCI=n
CONFIG_VHOST_USER_VGA=n
CONFIG_VIRTIO_VGA=n
CONFIG_VMWARE_VGA=n

# Displays
CONFIG_BOCHS_DISPLAY=n
CONFIG_DDC=n
CONFIG_QXL=n

# Graphics
CONFIG_OPENGL=n
CONFIG_SPICE=n
CONFIG_X11=n

# test devices
CONFIG_HYPERV_TESTDEV=n
CONFIG_ISA_TESTDEV=n
CONFIG_PCI_TESTDEV=n

# XEN
CONFIG_XEN=n

# PCIe
CONFIG_XIO3130=n

# SCSI
CONFIG_ESP=n
CONFIG_ESP_PCI=n
CONFIG_LSI_SCSI_PCI=n
CONFIG_MEGASAS_SCSI_PCI=n
CONFIG_MPTSAS_SCSI_PCI=n

# i2c
CONFIG_BITBANG_I2C=n

# UART
CONFIG_SERIAL_PCI_MULTI=n

# PCI
CONFIG_EDU=n
CONFIG_I82801B11=n
CONFIG_IOH3420=n
CONFIG_IPACK=n
CONFIG_PXB=n

# SD
CONFIG_SDHCI=n
CONFIG_SDHCI_PCI=n

# watchdog
CONFIG_WDT_IB6300ESB=n
CONFIG_WDT_IB700=n

# Apple
CONFIG_APPLESMC=n

# Timer
CONFIG_HPET=n

# IPMI
CONFIG_IPMI=n
CONFIG_IPMI_EXTERN=n
CONFIG_IPMI_LOCAL=n
CONFIG_PCI_IPMI_KCS=n
CONFIG_PCI_IPMI_BT=n
CONFIG_IPMI_SSIF=n

# misc
CONFIG_IVSHMEM_DEVICE=n
CONFIG_PVPANIC=n
CONFIG_SEV=n
CONFIG_SGA=n

#vhost
CONFIG_VHOST_USER_INPUT=n

# TPM
CONFIG_TPM_CRB=n
CONFIG_TPM_TIS=n
```


* `<https://wiki.qemu.org/Hosts/Linux>`_


