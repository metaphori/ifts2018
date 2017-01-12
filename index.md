---
layout: default
---

# Sistemi informatici e loro gestione

Si ricorda agli studenti che il materiale proposto è *consistentemente* più approfondito di quello visto a lezione.

La macchina virtuale utilizzata nel corso è disponibile [clickando qui](https://mega.nz/#!XMERGDwY!aIwNDUom-Fsi-Gy_8doA8IkT-qOpX3zdUZ4W0fcy_1s).

In caso di problemi (link mancanti, problemi di visualizzazione...) si prega di contattare direttamente [Danilo Pianini](mailto:danilo.pianini@unibo.it).

## Lezione 01: introduzione ai sistemi informatici

* [Introduzione all'informatica (in inglese)](01/intro.pdf)
* [Introduzione ai sistemi operativi](01/intro-os.pdf)

### Esempi di programmi

Stampa di `Ciaone` su terminale.

{% highlight c %}
#include<stdio.h>
int main(void)
{
    printf("Ciaone");
}
{% endhighlight %}

Stesso programma, scritto in assembler per Linux x86-64

{% highlight ca65 %}
.file	"test.c"
.section	.rodata
.LC0:
.string	"Ciaone"
.text
.globl	main
.type	main, @function
main:
.LFB0:
.cfi_startproc
pushq	%rbp
.cfi_def_cfa_offset 16
.cfi_offset 6, -16
movq	%rsp, %rbp
.cfi_def_cfa_register 6
movl	$.LC0, %edi
call	puts
movl	$0, %eax
popq	%rbp
.cfi_def_cfa 7, 8
ret
.cfi_endproc
.LFE0:
.size	main, .-main
.ident	"GCC: (GNU) 6.2.1 20160830"
.section	.note.GNU-stack,"",@progbits
{% endhighlight %}

Stesso programma, linguaggio macchina (esadecimale)

{% highlight hex %}
0000000 457f 464c 0102 0001 0000 0000 0000 0000
0000010 0002 003e 0001 0000 0400 0040 0000 0000
0000020 0040 0000 0000 0000 1940 0000 0000 0000
0000030 0000 0000 0040 0038 0009 0040 001e 001b
0000040 0006 0000 0005 0000 0040 0000 0000 0000
0000050 0040 0040 0000 0000 0040 0040 0000 0000
0000060 01f8 0000 0000 0000 01f8 0000 0000 0000
0000070 0008 0000 0000 0000 0003 0000 0004 0000
0000080 0238 0000 0000 0000 0238 0040 0000 0000
0000090 0238 0040 0000 0000 001c 0000 0000 0000
00000a0 001c 0000 0000 0000 0001 0000 0000 0000
00000b0 0001 0000 0005 0000 0000 0000 0000 0000
00000c0 0000 0040 0000 0000 0000 0040 0000 0000
00000d0 06c4 0000 0000 0000 06c4 0000 0000 0000
00000e0 0000 0020 0000 0000 0001 0000 0006 0000
00000f0 0e08 0000 0000 0000 0e08 0060 0000 0000
0000100 0e08 0060 0000 0000 0228 0000 0000 0000
0000110 0230 0000 0000 0000 0000 0020 0000 0000
0000120 0002 0000 0006 0000 0e20 0000 0000 0000
0000130 0e20 0060 0000 0000 0e20 0060 0000 0000
0000140 01d0 0000 0000 0000 01d0 0000 0000 0000
0000150 0008 0000 0000 0000 0004 0000 0004 0000
0000160 0254 0000 0000 0000 0254 0040 0000 0000
0000170 0254 0040 0000 0000 0044 0000 0000 0000
0000180 0044 0000 0000 0000 0004 0000 0000 0000
0000190 e550 6474 0004 0000 059c 0000 0000 0000
00001a0 059c 0040 0000 0000 059c 0040 0000 0000
00001b0 0034 0000 0000 0000 0034 0000 0000 0000
00001c0 0004 0000 0000 0000 e551 6474 0006 0000
00001d0 0000 0000 0000 0000 0000 0000 0000 0000
*
00001f0 0000 0000 0000 0000 0010 0000 0000 0000
0000200 e552 6474 0004 0000 0e08 0000 0000 0000
0000210 0e08 0060 0000 0000 0e08 0060 0000 0000
0000220 01f8 0000 0000 0000 01f8 0000 0000 0000
0000230 0001 0000 0000 0000 6c2f 6269 3436 6c2f
0000240 2d64 696c 756e 2d78 3878 2d36 3436 732e
0000250 2e6f 0032 0004 0000 0010 0000 0001 0000
0000260 4e47 0055 0000 0000 0002 0000 0006 0000
0000270 0020 0000 0004 0000 0014 0000 0003 0000
0000280 4e47 0055 b505 46cd b915 f782 b8a6 ad72
0000290 96ed 2169 f21c 69d9 0001 0000 0001 0000
00002a0 0001 0000 0000 0000 0000 0000 0000 0000
00002b0 0000 0000 0000 0000 0000 0000 0000 0000
*
00002d0 000b 0000 0012 0000 0000 0000 0000 0000
00002e0 0000 0000 0000 0000 0010 0000 0012 0000
00002f0 0000 0000 0000 0000 0000 0000 0000 0000
0000300 0022 0000 0020 0000 0000 0000 0000 0000
0000310 0000 0000 0000 0000 6c00 6269 2e63 6f73
0000320 362e 7000 7475 0073 5f5f 696c 6362 735f
0000330 6174 7472 6d5f 6961 006e 5f5f 6d67 6e6f
0000340 735f 6174 7472 5f5f 4700 494c 4342 325f
0000350 322e 352e 0000 0000 0002 0002 0000 0000
0000360 0001 0001 0001 0000 0010 0000 0000 0000
0000370 1a75 0969 0000 0002 0031 0000 0000 0000
0000380 0ff0 0060 0000 0000 0006 0000 0002 0000
0000390 0000 0000 0000 0000 0ff8 0060 0000 0000
00003a0 0006 0000 0003 0000 0000 0000 0000 0000
00003b0 1018 0060 0000 0000 0007 0000 0001 0000
00003c0 0000 0000 0000 0000 8348 08ec 8b48 2505
00003d0 200c 4800 c085 0274 d0ff 8348 08c4 00c3
00003e0 35ff 0c22 0020 25ff 0c24 0020 1f0f 0040
00003f0 25ff 0c22 0020 0068 0000 e900 ffe0 ffff
0000400 ed31 8949 5ed1 8948 48e2 e483 50f0 4954
0000410 c0c7 0580 0040 c748 10c1 4005 4800 c7c7
0000420 04f6 0040 15ff 0bc6 0020 0ff4 441f 0000
0000430 37b8 6010 5500 2d48 1030 0060 8348 0ef8
0000440 8948 76e5 b81b 0000 0000 8548 74c0 5d11
0000450 30bf 6010 ff00 66e0 1f0f 0084 0000 0000
0000460 c35d 1f0f 0040 2e66 1f0f 0084 0000 0000
0000470 30be 6010 5500 8148 30ee 6010 4800 fec1
0000480 4803 e589 8948 48f0 e8c1 483f c601 d148
0000490 74fe b815 0000 0000 8548 74c0 5d0b 30bf
00004a0 6010 ff00 0fe0 001f c35d 0f66 441f 0000
00004b0 3d80 0b79 0020 7500 5511 8948 e8e5 ff6e
00004c0 ffff c65d 6605 200b 0100 c3f3 1f0f 0040
00004d0 18bf 600e 4800 3f83 7500 eb05 0f93 001f
00004e0 00b8 0000 4800 c085 f174 4855 e589 d0ff
00004f0 e95d ff7a ffff 4855 e589 94bf 4005 e800
0000500 feec ffff f4eb 2e66 1f0f 0084 0000 0000
0000510 5741 5641 8941 41ff 4155 4c54 258d 08e6
0000520 0020 4855 2d8d 08e6 0020 4953 f689 8949
0000530 4cd5 e529 8348 08ec c148 03fd 87e8 fffe
0000540 48ff ed85 2074 db31 1f0f 0084 0000 0000
0000550 894c 4cea f689 8944 41ff 14ff 48dc c383
0000560 4801 dd39 ea75 8348 08c4 5d5b 5c41 5d41
0000570 5e41 5f41 90c3 2e66 1f0f 0084 0000 0000
0000580 c3f3 0000 8348 08ec 8348 08c4 00c3 0000
0000590 0001 0002 6943 6f61 656e 0000 1b01 3b03
00005a0 0030 0000 0005 0000 fe44 ffff 007c 0000
00005b0 fe64 ffff 004c 0000 ff5a ffff 00a4 0000
00005c0 ff74 ffff 00c4 0000 ffe4 ffff 010c 0000
00005d0 0014 0000 0000 0000 7a01 0052 7801 0110
00005e0 0c1b 0807 0190 1007 0014 0000 001c 0000
00005f0 fe10 ffff 002b 0000 0000 0000 0000 0000
0000600 0014 0000 0000 0000 7a01 0052 7801 0110
0000610 0c1b 0807 0190 0000 0024 0000 001c 0000
0000620 fdc0 ffff 0020 0000 0e00 4610 180e 0f4a
0000630 770b 8008 3f00 3b1a 332a 2224 0000 0000
0000640 001c 0000 0044 0000 feae ffff 0010 0000
0000650 4100 100e 0286 0d43 0006 0000 0000 0000
0000660 0044 0000 0064 0000 fea8 ffff 0065 0000
0000670 4200 100e 028f 0e42 8e18 4503 200e 048d
0000680 0e42 8c28 4805 300e 0686 0e48 8338 4d07
0000690 400e 0e72 4138 300e 0e41 4228 200e 0e42
00006a0 4218 100e 0e42 0008 0014 0000 00ac 0000
00006b0 fed0 ffff 0002 0000 0000 0000 0000 0000
00006c0 0000 0000 0000 0000 0000 0000 0000 0000
*
0000e00 0000 0000 0000 0000 04d0 0040 0000 0000
0000e10 04b0 0040 0000 0000 0000 0000 0000 0000
0000e20 0001 0000 0000 0000 0001 0000 0000 0000
0000e30 000c 0000 0000 0000 03c8 0040 0000 0000
0000e40 000d 0000 0000 0000 0584 0040 0000 0000
0000e50 0019 0000 0000 0000 0e08 0060 0000 0000
0000e60 001b 0000 0000 0000 0008 0000 0000 0000
0000e70 001a 0000 0000 0000 0e10 0060 0000 0000
0000e80 001c 0000 0000 0000 0008 0000 0000 0000
0000e90 fef5 6fff 0000 0000 0298 0040 0000 0000
0000ea0 0005 0000 0000 0000 0318 0040 0000 0000
0000eb0 0006 0000 0000 0000 02b8 0040 0000 0000
0000ec0 000a 0000 0000 0000 003d 0000 0000 0000
0000ed0 000b 0000 0000 0000 0018 0000 0000 0000
0000ee0 0015 0000 0000 0000 0000 0000 0000 0000
0000ef0 0003 0000 0000 0000 1000 0060 0000 0000
0000f00 0002 0000 0000 0000 0018 0000 0000 0000
0000f10 0014 0000 0000 0000 0007 0000 0000 0000
0000f20 0017 0000 0000 0000 03b0 0040 0000 0000
0000f30 0007 0000 0000 0000 0380 0040 0000 0000
0000f40 0008 0000 0000 0000 0030 0000 0000 0000
0000f50 0009 0000 0000 0000 0018 0000 0000 0000
0000f60 fffe 6fff 0000 0000 0360 0040 0000 0000
0000f70 ffff 6fff 0000 0000 0001 0000 0000 0000
0000f80 fff0 6fff 0000 0000 0356 0040 0000 0000
0000f90 0000 0000 0000 0000 0000 0000 0000 0000
*
0001000 0e20 0060 0000 0000 0000 0000 0000 0000
0001010 0000 0000 0000 0000 03f6 0040 0000 0000
0001020 0000 0000 0000 0000 0000 0000 0000 0000
0001030 4347 3a43 2820 4e47 2955 3620 312e 312e
0001040 3220 3130 3036 3038 0032 4347 3a43 2820
0001050 4e47 2955 3620 322e 312e 3220 3130 3036
0001060 3338 0030 0000 0000 0000 0000 0000 0000
0001070 0000 0000 0000 0000 0000 0000 0000 0000
0001080 0000 0000 0003 0001 0238 0040 0000 0000
0001090 0000 0000 0000 0000 0000 0000 0003 0002
00010a0 0254 0040 0000 0000 0000 0000 0000 0000
00010b0 0000 0000 0003 0003 0274 0040 0000 0000
00010c0 0000 0000 0000 0000 0000 0000 0003 0004
00010d0 0298 0040 0000 0000 0000 0000 0000 0000
00010e0 0000 0000 0003 0005 02b8 0040 0000 0000
00010f0 0000 0000 0000 0000 0000 0000 0003 0006
0001100 0318 0040 0000 0000 0000 0000 0000 0000
0001110 0000 0000 0003 0007 0356 0040 0000 0000
0001120 0000 0000 0000 0000 0000 0000 0003 0008
0001130 0360 0040 0000 0000 0000 0000 0000 0000
0001140 0000 0000 0003 0009 0380 0040 0000 0000
0001150 0000 0000 0000 0000 0000 0000 0003 000a
0001160 03b0 0040 0000 0000 0000 0000 0000 0000
0001170 0000 0000 0003 000b 03c8 0040 0000 0000
0001180 0000 0000 0000 0000 0000 0000 0003 000c
0001190 03e0 0040 0000 0000 0000 0000 0000 0000
00011a0 0000 0000 0003 000d 0400 0040 0000 0000
00011b0 0000 0000 0000 0000 0000 0000 0003 000e
00011c0 0584 0040 0000 0000 0000 0000 0000 0000
00011d0 0000 0000 0003 000f 0590 0040 0000 0000
00011e0 0000 0000 0000 0000 0000 0000 0003 0010
00011f0 059c 0040 0000 0000 0000 0000 0000 0000
0001200 0000 0000 0003 0011 05d0 0040 0000 0000
0001210 0000 0000 0000 0000 0000 0000 0003 0012
0001220 0e08 0060 0000 0000 0000 0000 0000 0000
0001230 0000 0000 0003 0013 0e10 0060 0000 0000
0001240 0000 0000 0000 0000 0000 0000 0003 0014
0001250 0e18 0060 0000 0000 0000 0000 0000 0000
0001260 0000 0000 0003 0015 0e20 0060 0000 0000
0001270 0000 0000 0000 0000 0000 0000 0003 0016
0001280 0ff0 0060 0000 0000 0000 0000 0000 0000
0001290 0000 0000 0003 0017 1000 0060 0000 0000
00012a0 0000 0000 0000 0000 0000 0000 0003 0018
00012b0 1020 0060 0000 0000 0000 0000 0000 0000
00012c0 0000 0000 0003 0019 1030 0060 0000 0000
00012d0 0000 0000 0000 0000 0000 0000 0003 001a
00012e0 0000 0000 0000 0000 0000 0000 0000 0000
00012f0 0001 0000 0004 fff1 0000 0000 0000 0000
0001300 0000 0000 0000 0000 0008 0000 0004 fff1
0001310 0000 0000 0000 0000 0000 0000 0000 0000
0001320 0013 0000 0001 0014 0e18 0060 0000 0000
0001330 0000 0000 0000 0000 0020 0000 0002 000d
0001340 0430 0040 0000 0000 0000 0000 0000 0000
0001350 0022 0000 0002 000d 0470 0040 0000 0000
0001360 0000 0000 0000 0000 0035 0000 0002 000d
0001370 04b0 0040 0000 0000 0000 0000 0000 0000
0001380 004b 0000 0001 0019 1030 0060 0000 0000
0001390 0001 0000 0000 0000 005a 0000 0001 0013
00013a0 0e10 0060 0000 0000 0000 0000 0000 0000
00013b0 0081 0000 0002 000d 04d0 0040 0000 0000
00013c0 0000 0000 0000 0000 008d 0000 0001 0012
00013d0 0e08 0060 0000 0000 0000 0000 0000 0000
00013e0 00ac 0000 0004 fff1 0000 0000 0000 0000
00013f0 0000 0000 0000 0000 0008 0000 0004 fff1
0001400 0000 0000 0000 0000 0000 0000 0000 0000
0001410 00b3 0000 0001 0011 06c0 0040 0000 0000
0001420 0000 0000 0000 0000 00c1 0000 0001 0014
0001430 0e18 0060 0000 0000 0000 0000 0000 0000
0001440 0000 0000 0004 fff1 0000 0000 0000 0000
0001450 0000 0000 0000 0000 00cd 0000 0000 0012
0001460 0e10 0060 0000 0000 0000 0000 0000 0000
0001470 00de 0000 0001 0015 0e20 0060 0000 0000
0001480 0000 0000 0000 0000 00e7 0000 0000 0012
0001490 0e08 0060 0000 0000 0000 0000 0000 0000
00014a0 00fa 0000 0000 0010 059c 0040 0000 0000
00014b0 0000 0000 0000 0000 010d 0000 0001 0017
00014c0 1000 0060 0000 0000 0000 0000 0000 0000
00014d0 0123 0000 0012 000d 0580 0040 0000 0000
00014e0 0002 0000 0000 0000 016d 0000 0020 0018
00014f0 1020 0060 0000 0000 0000 0000 0000 0000
0001500 0133 0000 0012 0000 0000 0000 0000 0000
0001510 0000 0000 0000 0000 0145 0000 0010 0018
0001520 1030 0060 0000 0000 0000 0000 0000 0000
0001530 012d 0000 0012 000e 0584 0040 0000 0000
0001540 0000 0000 0000 0000 014c 0000 0012 0000
0001550 0000 0000 0000 0000 0000 0000 0000 0000
0001560 016b 0000 0010 0018 1020 0060 0000 0000
0001570 0000 0000 0000 0000 0178 0000 0020 0000
0001580 0000 0000 0000 0000 0000 0000 0000 0000
0001590 0187 0000 0211 0018 1028 0060 0000 0000
00015a0 0000 0000 0000 0000 0194 0000 0011 000f
00015b0 0590 0040 0000 0000 0004 0000 0000 0000
00015c0 01a3 0000 0012 000d 0510 0040 0000 0000
00015d0 0065 0000 0000 0000 00d9 0000 0010 0019
00015e0 1038 0060 0000 0000 0000 0000 0000 0000
00015f0 0171 0000 0012 000d 0400 0040 0000 0000
0001600 002b 0000 0000 0000 01b3 0000 0010 0019
0001610 1030 0060 0000 0000 0000 0000 0000 0000
0001620 01bf 0000 0012 000d 04f6 0040 0000 0000
0001630 0010 0000 0000 0000 01c4 0000 0211 0018
0001640 1030 0060 0000 0000 0000 0000 0000 0000
0001650 01ad 0000 0012 000b 03c8 0040 0000 0000
0001660 0000 0000 0000 0000 6900 696e 2e74 0063
0001670 7263 7374 7574 6666 632e 5f00 4a5f 5243
0001680 4c5f 5349 5f54 005f 6564 6572 6967 7473
0001690 7265 745f 5f6d 6c63 6e6f 7365 5f00 645f
00016a0 5f6f 6c67 626f 6c61 645f 6f74 7372 615f
00016b0 7875 6300 6d6f 6c70 7465 6465 362e 3139
00016c0 0036 5f5f 6f64 675f 6f6c 6162 5f6c 7464
00016d0 726f 5f73 7561 5f78 6966 696e 615f 7272
00016e0 7961 655f 746e 7972 6600 6172 656d 645f
00016f0 6d75 796d 5f00 665f 6172 656d 645f 6d75
0001700 796d 695f 696e 5f74 7261 6172 5f79 6e65
0001710 7274 0079 6574 7473 632e 5f00 465f 4152
0001720 454d 455f 444e 5f5f 5f00 4a5f 5243 455f
0001730 444e 5f5f 5f00 695f 696e 5f74 7261 6172
0001740 5f79 6e65 0064 445f 4e59 4d41 4349 5f00
0001750 695f 696e 5f74 7261 6172 5f79 7473 7261
0001760 0074 5f5f 4e47 5f55 4845 465f 4152 454d
0001770 485f 5244 5f00 4c47 424f 4c41 4f5f 4646
0001780 4553 5f54 4154 4c42 5f45 5f00 6c5f 6269
0001790 5f63 7363 5f75 6966 696e 7000 7475 4073
00017a0 4740 494c 4342 325f 322e 352e 5f00 6465
00017b0 7461 0061 5f5f 696c 6362 735f 6174 7472
00017c0 6d5f 6961 406e 4740 494c 4342 325f 322e
00017d0 352e 5f00 645f 7461 5f61 7473 7261 0074
00017e0 5f5f 6d67 6e6f 735f 6174 7472 5f5f 5f00
00017f0 645f 6f73 685f 6e61 6c64 0065 495f 5f4f
0001800 7473 6964 5f6e 7375 6465 5f00 6c5f 6269
0001810 5f63 7363 5f75 6e69 7469 5f00 625f 7373
0001820 735f 6174 7472 6d00 6961 006e 5f5f 4d54
0001830 5f43 4e45 5f44 005f 2e00 7973 746d 6261
0001840 2e00 7473 7472 6261 2e00 6873 7473 7472
0001850 6261 2e00 6e69 6574 7072 2e00 6f6e 6574
0001860 412e 4942 742d 6761 2e00 6f6e 6574 672e
0001870 756e 622e 6975 646c 692d 0064 672e 756e
0001880 682e 7361 0068 642e 6e79 7973 006d 642e
0001890 6e79 7473 0072 672e 756e 762e 7265 6973
00018a0 6e6f 2e00 6e67 2e75 6576 7372 6f69 5f6e
00018b0 0072 722e 6c65 2e61 7964 006e 722e 6c65
00018c0 2e61 6c70 0074 692e 696e 0074 742e 7865
00018d0 0074 662e 6e69 0069 722e 646f 7461 0061
00018e0 652e 5f68 7266 6d61 5f65 6468 0072 652e
00018f0 5f68 7266 6d61 0065 692e 696e 5f74 7261
0001900 6172 0079 662e 6e69 5f69 7261 6172 0079
0001910 6a2e 7263 2e00 7964 616e 696d 0063 672e
0001920 746f 2e00 6f67 2e74 6c70 0074 642e 7461
0001930 0061 622e 7373 2e00 6f63 6d6d 6e65 0074
0001940 0000 0000 0000 0000 0000 0000 0000 0000
*
0001980 001b 0000 0001 0000 0002 0000 0000 0000
0001990 0238 0040 0000 0000 0238 0000 0000 0000
00019a0 001c 0000 0000 0000 0000 0000 0000 0000
00019b0 0001 0000 0000 0000 0000 0000 0000 0000
00019c0 0023 0000 0007 0000 0002 0000 0000 0000
00019d0 0254 0040 0000 0000 0254 0000 0000 0000
00019e0 0020 0000 0000 0000 0000 0000 0000 0000
00019f0 0004 0000 0000 0000 0000 0000 0000 0000
0001a00 0031 0000 0007 0000 0002 0000 0000 0000
0001a10 0274 0040 0000 0000 0274 0000 0000 0000
0001a20 0024 0000 0000 0000 0000 0000 0000 0000
0001a30 0004 0000 0000 0000 0000 0000 0000 0000
0001a40 0044 0000 fff6 6fff 0002 0000 0000 0000
0001a50 0298 0040 0000 0000 0298 0000 0000 0000
0001a60 001c 0000 0000 0000 0005 0000 0000 0000
0001a70 0008 0000 0000 0000 0000 0000 0000 0000
0001a80 004e 0000 000b 0000 0002 0000 0000 0000
0001a90 02b8 0040 0000 0000 02b8 0000 0000 0000
0001aa0 0060 0000 0000 0000 0006 0000 0001 0000
0001ab0 0008 0000 0000 0000 0018 0000 0000 0000
0001ac0 0056 0000 0003 0000 0002 0000 0000 0000
0001ad0 0318 0040 0000 0000 0318 0000 0000 0000
0001ae0 003d 0000 0000 0000 0000 0000 0000 0000
0001af0 0001 0000 0000 0000 0000 0000 0000 0000
0001b00 005e 0000 ffff 6fff 0002 0000 0000 0000
0001b10 0356 0040 0000 0000 0356 0000 0000 0000
0001b20 0008 0000 0000 0000 0005 0000 0000 0000
0001b30 0002 0000 0000 0000 0002 0000 0000 0000
0001b40 006b 0000 fffe 6fff 0002 0000 0000 0000
0001b50 0360 0040 0000 0000 0360 0000 0000 0000
0001b60 0020 0000 0000 0000 0006 0000 0001 0000
0001b70 0008 0000 0000 0000 0000 0000 0000 0000
0001b80 007a 0000 0004 0000 0002 0000 0000 0000
0001b90 0380 0040 0000 0000 0380 0000 0000 0000
0001ba0 0030 0000 0000 0000 0005 0000 0000 0000
0001bb0 0008 0000 0000 0000 0018 0000 0000 0000
0001bc0 0084 0000 0004 0000 0042 0000 0000 0000
0001bd0 03b0 0040 0000 0000 03b0 0000 0000 0000
0001be0 0018 0000 0000 0000 0005 0000 0017 0000
0001bf0 0008 0000 0000 0000 0018 0000 0000 0000
0001c00 008e 0000 0001 0000 0006 0000 0000 0000
0001c10 03c8 0040 0000 0000 03c8 0000 0000 0000
0001c20 0017 0000 0000 0000 0000 0000 0000 0000
0001c30 0004 0000 0000 0000 0000 0000 0000 0000
0001c40 0089 0000 0001 0000 0006 0000 0000 0000
0001c50 03e0 0040 0000 0000 03e0 0000 0000 0000
0001c60 0020 0000 0000 0000 0000 0000 0000 0000
0001c70 0010 0000 0000 0000 0010 0000 0000 0000
0001c80 0094 0000 0001 0000 0006 0000 0000 0000
0001c90 0400 0040 0000 0000 0400 0000 0000 0000
0001ca0 0182 0000 0000 0000 0000 0000 0000 0000
0001cb0 0010 0000 0000 0000 0000 0000 0000 0000
0001cc0 009a 0000 0001 0000 0006 0000 0000 0000
0001cd0 0584 0040 0000 0000 0584 0000 0000 0000
0001ce0 0009 0000 0000 0000 0000 0000 0000 0000
0001cf0 0004 0000 0000 0000 0000 0000 0000 0000
0001d00 00a0 0000 0001 0000 0002 0000 0000 0000
0001d10 0590 0040 0000 0000 0590 0000 0000 0000
0001d20 000b 0000 0000 0000 0000 0000 0000 0000
0001d30 0004 0000 0000 0000 0000 0000 0000 0000
0001d40 00a8 0000 0001 0000 0002 0000 0000 0000
0001d50 059c 0040 0000 0000 059c 0000 0000 0000
0001d60 0034 0000 0000 0000 0000 0000 0000 0000
0001d70 0004 0000 0000 0000 0000 0000 0000 0000
0001d80 00b6 0000 0001 0000 0002 0000 0000 0000
0001d90 05d0 0040 0000 0000 05d0 0000 0000 0000
0001da0 00f4 0000 0000 0000 0000 0000 0000 0000
0001db0 0008 0000 0000 0000 0000 0000 0000 0000
0001dc0 00c0 0000 000e 0000 0003 0000 0000 0000
0001dd0 0e08 0060 0000 0000 0e08 0000 0000 0000
0001de0 0008 0000 0000 0000 0000 0000 0000 0000
0001df0 0008 0000 0000 0000 0008 0000 0000 0000
0001e00 00cc 0000 000f 0000 0003 0000 0000 0000
0001e10 0e10 0060 0000 0000 0e10 0000 0000 0000
0001e20 0008 0000 0000 0000 0000 0000 0000 0000
0001e30 0008 0000 0000 0000 0008 0000 0000 0000
0001e40 00d8 0000 0001 0000 0003 0000 0000 0000
0001e50 0e18 0060 0000 0000 0e18 0000 0000 0000
0001e60 0008 0000 0000 0000 0000 0000 0000 0000
*
0001e80 00dd 0000 0006 0000 0003 0000 0000 0000
0001e90 0e20 0060 0000 0000 0e20 0000 0000 0000
0001ea0 01d0 0000 0000 0000 0006 0000 0000 0000
0001eb0 0008 0000 0000 0000 0010 0000 0000 0000
0001ec0 00e6 0000 0001 0000 0003 0000 0000 0000
0001ed0 0ff0 0060 0000 0000 0ff0 0000 0000 0000
0001ee0 0010 0000 0000 0000 0000 0000 0000 0000
0001ef0 0008 0000 0000 0000 0008 0000 0000 0000
0001f00 00eb 0000 0001 0000 0003 0000 0000 0000
0001f10 1000 0060 0000 0000 1000 0000 0000 0000
0001f20 0020 0000 0000 0000 0000 0000 0000 0000
0001f30 0008 0000 0000 0000 0008 0000 0000 0000
0001f40 00f4 0000 0001 0000 0003 0000 0000 0000
0001f50 1020 0060 0000 0000 1020 0000 0000 0000
0001f60 0010 0000 0000 0000 0000 0000 0000 0000
0001f70 0008 0000 0000 0000 0000 0000 0000 0000
0001f80 00fa 0000 0008 0000 0003 0000 0000 0000
0001f90 1030 0060 0000 0000 1030 0000 0000 0000
0001fa0 0008 0000 0000 0000 0000 0000 0000 0000
0001fb0 0001 0000 0000 0000 0000 0000 0000 0000
0001fc0 00ff 0000 0001 0000 0030 0000 0000 0000
0001fd0 0000 0000 0000 0000 1030 0000 0000 0000
0001fe0 0034 0000 0000 0000 0000 0000 0000 0000
0001ff0 0001 0000 0000 0000 0001 0000 0000 0000
0002000 0011 0000 0003 0000 0000 0000 0000 0000
0002010 0000 0000 0000 0000 1838 0000 0000 0000
0002020 0108 0000 0000 0000 0000 0000 0000 0000
0002030 0001 0000 0000 0000 0000 0000 0000 0000
0002040 0001 0000 0002 0000 0000 0000 0000 0000
0002050 0000 0000 0000 0000 1068 0000 0000 0000
0002060 0600 0000 0000 0000 001d 0000 002f 0000
0002070 0008 0000 0000 0000 0018 0000 0000 0000
0002080 0009 0000 0003 0000 0000 0000 0000 0000
0002090 0000 0000 0000 0000 1668 0000 0000 0000
00020a0 01d0 0000 0000 0000 0000 0000 0000 0000
00020b0 0001 0000 0000 0000 0000 0000 0000 0000
00020c0
{% endhighlight %}

Programma C che si "inloopa" (ciclo infinito)

{% highlight c %}
#include<stdio.h>
int main(void)
{
    while (1) {
        printf("Ciaone");
    }
}
{% endhighlight %}

## Lezione 02: sistemi operativi e processi

* [Architettura dei sistemi operativi](02/architettura.pdf)
* [Struttura dei sistemi operativi](02/struttura.pdf)
* [I processi](02/processi.pdf)

### Simboli utili:

* Tilde: `~` (Alt destro + ì)
* Underscore: `_`
* Sharp: `#`
* At: `@`
* Slash: `/`
* Backslash: `\`

### Uso veloce del terminale `bash`

* Freccia su: richiama il comando precedente
* Freccia giù: richiama il comando successivo (se presente)
* TAB: autocompleta il comando o il percorso corrente (solo se esiste un'unica opzione disponibile)
* Doppio TAB: mostra tutti i possibile autocompletamenti
  * Nel caso in cui non vi sia alcuna possibilità, non mostra nulla
  * Nel caso in cui vi siano moltissime possibilità, chiede prima conferma della volontà di mostrarle tutte

## Lezione 03: file system e `bash`

* [Il file system](03/fs.pdf)