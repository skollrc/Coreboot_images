# Note for Tianocore
If you had a classical bios install before moving to tinocore, use a Debian live image (or any other disto) and do this:

```
sudo apt-get install -y grub-efi-amd64
sudo mount /dev/sda1 /mnt
sudo mkdir -p /mnt/boot/efi
sudo mount /dev/sda3 /mnt/boot/efi
for d in dev sys proc usr run; do sudo mount -B /$d /mnt/$d; done
sudo modprobe efivars
sudo chroot /mnt
grub-install --target=x86_64-efi --efi-directory=/boot/efi --bootloader-id=ubuntu --recheck --no-floppy --debug
```

Then reboot and it shold work

# Seabios image content
This image contains the following sections that can be manipulated with this tool:

'RW_MRC_CACHE' (size 65536, offset 11534336)
'COREBOOT' (CBFS, size 982528, offset 11600384)

It is possible to perform either the write action or the CBFS add/remove actions on every section listed above.
To see the image's read-only sections as well, rerun with the -w option.
    CBFSPRINT  coreboot.rom

FMAP REGION: COREBOOT
Name                           Offset     Type           Size   Comp
* cbfs master header             0x0        cbfs header        32 none
* fallback/romstage              0x80       stage           80268 none
* fallback/ramstage              0x13a80    stage          115318 none
* vgaroms/seavgabios.bin         0x2fd40    raw             27136 none
* config                         0x367c0    raw               476 none
* revision                       0x36a00    raw               675 none
* cmos.default                   0x36d00    cmos_default      256 none
* cmos_layout.bin                0x36e40    cmos_layout      1804 none
* fallback/postcar               0x375c0    stage           19252 none
* fallback/dsdt.aml              0x3c140    raw             14768 none
* img/nvramcui                   0x3fb40    simple elf      67825 none
* fallback/payload               0x50480    simple elf      67315 none
* payload_config                 0x60bc0    raw              1700 none
* payload_revision               0x612c0    raw               235 none
* img/memtest                    0x61400    simple elf      47497 none
* etc/ps2-keyboard-spinup        0x6cdc0    raw                 8 none
* (empty)                        0x6ce00    null           533464 none
* bootblock                      0xef200    bootblock        3016 none
    HOSTCC     cbfstool/ifwitool.o
    HOSTCC     cbfstool/ifwitool (link)

