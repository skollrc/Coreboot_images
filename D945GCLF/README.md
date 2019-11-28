This image contains the following sections that can be manipulated with this tool:

'COREBOOT' (CBFS, size 523776, offset 512)

It is possible to perform either the write action or the CBFS add/remove actions on every section listed above.
To see the image's read-only sections as well, rerun with the -w option.
    CBFSPRINT  coreboot.rom

FMAP REGION: COREBOOT
Name                           Offset     Type           Size   Comp
* cbfs master header             0x0        cbfs header        32 none
* fallback/romstage              0x80       stage           44196 none
* fallback/ramstage              0xadc0     stage           86860 none
* vgaroms/seavgabios.bin         0x20180    raw             28672 none
* config                         0x27200    raw               168 none
* revision                       0x27300    raw               674 none
* vbt.bin                        0x27600    raw               802 LZMA (1790 decompressed)
* cmos_layout.bin                0x27980    cmos_layout      1128 none
*fallback/postcar               0x27e40    stage           18532 none
* fallback/dsdt.aml              0x2c700    raw              9140 none
* fallback/payload               0x2eb00    simple elf      69435 none
* payload_config                 0x3fa80    raw              1710 none
* payload_revision               0x40180    raw               238 none
* (empty)                        0x402c0    null           244440 none
* bootblock                      0x7bdc0    bootblock       16384 none
    HOSTCC     cbfstool/ifwitool.o
    HOSTCC     cbfstool/ifwitool (link)

Built intel/d945gclf (D945GCLF)

