# Intel D510MO

**This image is blob free except micro-code (needed even in libreboot)

# Test board specs

CPU: Atom D510 more info on [ark](https://ark.intel.com/content/www/us/en/ark/products/43098/intel-atom-processor-d510-1m-cache-1-66-ghz.html "Atom D510 ark")
RAM: ADATA 2x2Go DDR2 800
mPCIe extension card:  IOCREST 4 ports SATA III 6G Mini PCI Express Marvel 88SE9215
SSD: 120Gb Sandisk
HDD: 6Tb WD Red + 4x3Tb WD Red RAID 5 mdam
OS: OMV 4.1.22-amd64 more info [here](https://www.openmediavault.org/ "OMV official website")


# Image content

This image contains the following sections that can be manipulated with this tool:

'COREBOOT' (CBFS, size 1048064, offset 512)

It is possible to perform either the write action or the CBFS add/remove actions on every section listed above.
To see the image's read-only sections as well, rerun with the -w option.
    CBFSPRINT  coreboot.rom

FMAP REGION: COREBOOT
Name                           Offset     Type           Size   Comp
cbfs master header             0x0        cbfs header        32 none
fallback/romstage              0x80       stage           42428 none
fallback/ramstage              0x13340    stage           75711 none
vgaroms/seavgabios.bin         0x25b40    raw             28672 none
config                         0x2cbc0    raw               133 none
revision                       0x2cc80    raw               674 none
cmos_layout.bin                0x2cf80    cmos_layout       968 none
fallback/postcar               0x2d380    stage           18464 none
fallback/dsdt.aml              0x31c00    raw              7799 none
fallback/payload               0x33ac0    simple elf      69435 none
payload_config                 0x44a40    raw              1710 none
payload_revision               0x45140    raw               238 none
(empty)                        0x45280    null           699160 none
bootblock                      0xefdc0    bootblock       65536 none

Built intel/d510mo (D510MO)

