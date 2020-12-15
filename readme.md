<h1>Tradfri gateway on an Edgerouter POE/5</h1>

root@egx:~# tcpdump -n -i eth1 -vvvv
tcpdump: listening on eth1, link-type EN10MB (Ethernet), capture size 262144 bytes
17:38:48.960380 IP6 (hlim 1, next-header Options (0) payload length: 96) fe80::f29f:c2ff:fe17:704c > ff02::16: HBH (rtalert: 0                                                                                                                                                              x0000) (padn) [icmp6 sum ok] ICMP6, multicast listener report v2, 4 group record(s) [gaddr ff02::fb to_ex { }] [gaddr ff02::1:                                                                                                                                                              ff00:0 to_ex { }] [gaddr ff02::1:ff17:704c to_ex { }] [gaddr ff02::2 to_ex { }]
17:38:49.810334 IP6 (hlim 1, next-header Options (0) payload length: 96) fe80::f29f:c2ff:fe17:704c > ff02::16: HBH (rtalert: 0                                                                                                                                                              x0000) (padn) [icmp6 sum ok] ICMP6, multicast listener report v2, 4 group record(s) [gaddr ff02::fb to_ex { }] [gaddr ff02::1:                                                                                                                                                              ff00:0 to_ex { }] [gaddr ff02::1:ff17:704c to_ex { }] [gaddr ff02::2 to_ex { }]
17:39:04.056844 IP (tos 0x0, ttl 255, id 52167, offset 0, flags [DF], proto UDP (17), length 68)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0 PTR (QM)? _googlecast._tcp.local. (40)
17:39:04.061317 IP (tos 0x0, ttl 255, id 52168, offset 0, flags [DF], proto UDP (17), length 118)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0 SRV (QM)? google-nest-mini-e8b58877627a8cea281b68f6f4a17d69._googlecast._                                                                                                                                                              tcp.local. (90)
17:39:04.064590 IP (tos 0x0, ttl 255, id 52169, offset 0, flags [DF], proto UDP (17), length 398)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 4/0/0 _googlecast._tcp.local. [2m] PTR Google-Nest-Mini-e8b5887762                                                                                                                                                              7a8cea281b68f6f4a17d69._googlecast._tcp.local., e8b58877-627a-8cea-281b-68f6f4a17d69.local. (Cache flush) [2m] A 172.17.114.31                                                                                                                                                              , Google-Nest-Mini-e8b58877627a8cea281b68f6f4a17d69._googlecast._tcp.local. (Cache flush) [2m] SRV e8b58877-627a-8cea-281b-68f                                                                                                                                                              6f4a17d69.local.:8009 0 0, Google-Nest-Mini-e8b58877627a8cea281b68f6f4a17d69._googlecast._tcp.local. (Cache flush) [1h15m] TXT                                                                                                                                                               "id=e8b58877627a8cea281b68f6f4a17d69" "cd=C4D26B8C90E081C1D8DB77EB7294BDA9" "rm=6A07C12CBEA61E31" "ve=05" "md=Google Nest Min                                                                                                                                                              i" "ic=/setup/icon.png" "fn=Zolder" "ca=198660" "st=0" "bs=FA8FCA706ACF" "nf=1" "rs=" (370)
17:39:04.069574 IP (tos 0x0, ttl 255, id 52170, offset 0, flags [DF], proto UDP (17), length 118)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0 SRV (QM)? chromecast-audio-342ddd4343722cdfd284401f9284f6b0._googlecast._                                                                                                                                                              tcp.local. (90)
17:39:04.073814 IP (tos 0x0, ttl 255, id 52171, offset 0, flags [DF], proto UDP (17), length 121)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0 SRV (QM)? google-cast-group-f7934384f50f411d8f15dcf8ab39b5e2-1._googlecas                                                                                                                                                              t._tcp.local. (93)
17:39:04.077400 IP (tos 0x0, ttl 255, id 52172, offset 0, flags [DF], proto UDP (17), length 121)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0 SRV (QM)? google-cast-group-93d01926c9e04458b6bc515a347c3ecc-1._googlecas                                                                                                                                                              t._tcp.local. (93)
17:39:04.081962 IP (tos 0x0, ttl 255, id 52173, offset 0, flags [DF], proto UDP (17), length 121)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0 SRV (QM)? google-cast-group-e63b80d728e44ebf9ba30ce60e73e8ff-1._googlecas                                                                                                                                                              t._tcp.local. (93)
17:39:04.092166 IP (tos 0x0, ttl 255, id 52174, offset 0, flags [DF], proto UDP (17), length 390)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 4/0/0 _googlecast._tcp.local. [2m] PTR Nest-Audio-5fd01e95241ca3d6                                                                                                                                                              277f62eb6326b954._googlecast._tcp.local., 5fd01e95-241c-a3d6-277f-62eb6326b954.local. (Cache flush) [2m] A 172.17.114.24, Nest                                                                                                                                                              -Audio-5fd01e95241ca3d6277f62eb6326b954._googlecast._tcp.local. (Cache flush) [2m] SRV 5fd01e95-241c-a3d6-277f-62eb6326b954.lo                                                                                                                                                              cal.:8009 0 0, Nest-Audio-5fd01e95241ca3d6277f62eb6326b954._googlecast._tcp.local. (Cache flush) [1h15m] TXT "id=5fd01e95241ca                                                                                                                                                              3d6277f62eb6326b954" "cd=6B0130740790B7044ED2EA5C3CB07A7B" "rm=8B094BD64BF5D14E" "ve=05" "md=Nest Audio" "ic=/setup/icon.png"                                                                                                                                                               "fn=Slaapkamer" "ca=198660" "st=0" "bs=FA8FCA60A82E" "nf=1" "rs=" (362)
17:39:04.095821 IP (tos 0x0, ttl 255, id 52175, offset 0, flags [DF], proto UDP (17), length 391)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 3/0/0 _googlecast._tcp.local. [2m] PTR Google-Cast-Group-b4389908a                                                                                                                                                              b674809a8b9f02e3ccc711c._googlecast._tcp.local., Google-Cast-Group-b4389908ab674809a8b9f02e3ccc711c._googlecast._tcp.local. (C                                                                                                                                                              ache flush) [2m] SRV 5fd01e95-241c-a3d6-277f-62eb6326b954.local.:32162 0 0, Google-Cast-Group-b4389908ab674809a8b9f02e3ccc711c                                                                                                                                                              ._googlecast._tcp.local. (Cache flush) [1h15m] TXT "id=b4389908-ab67-4809-a8b9-f02e3ccc711c" "cd=b4389908-ab67-4809-a8b9-f02e3                                                                                                                                                              ccc711c" "rm=8B094BD64BF5D14E" "ve=05" "md=Google Cast Group" "ic=/setup/icon.png" "fn=Boven" "ca=198692" "st=0" "bs=FA8FCA60A                                                                                                                                                              82E" "nf=1" "rs=" (363)
17:39:04.110951 IP (tos 0x0, ttl 255, id 52176, offset 0, flags [DF], proto UDP (17), length 424)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 4/0/0 _googlecast._tcp.local. [2m] PTR Chromecast-Audio-342ddd4343                                                                                                                                                              722cdfd284401f9284f6b0._googlecast._tcp.local., 342ddd43-4372-2cdf-d284-401f9284f6b0.local. (Cache flush) [2m] A 172.17.114.18                                                                                                                                                              , Chromecast-Audio-342ddd4343722cdfd284401f9284f6b0._googlecast._tcp.local. (Cache flush) [2m] SRV 342ddd43-4372-2cdf-d284-401                                                                                                                                                              f9284f6b0.local.:8009 0 0, Chromecast-Audio-342ddd4343722cdfd284401f9284f6b0._googlecast._tcp.local. (Cache flush) [1h15m] TXT                                                                                                                                                               "id=342ddd4343722cdfd284401f9284f6b0" "cd=D44812348A098CDF225570FC4FBA7F1A" "rm=88C28054F189A25C" "ve=05" "md=Chromecast Audi                                                                                                                                                              o" "ic=/setup/icon.png" "fn=AudioPro" "ca=198660" "st=1" "bs=FA8FCA8D5534" "nf=1" "rs=Casting: Forever Distant" (396)
17:39:04.116483 IP (tos 0x0, ttl 255, id 52177, offset 0, flags [DF], proto UDP (17), length 426)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 3/0/0 _googlecast._tcp.local. [2m] PTR Google-Cast-Group-f7934384f                                                                                                                                                              50f411d8f15dcf8ab39b5e2-1._googlecast._tcp.local., Google-Cast-Group-f7934384f50f411d8f15dcf8ab39b5e2-1._googlecast._tcp.local                                                                                                                                                              . (Cache flush) [2m] SRV 342ddd43-4372-2cdf-d284-401f9284f6b0.local.:32901 0 0, Google-Cast-Group-f7934384f50f411d8f15dcf8ab39                                                                                                                                                              b5e2-1._googlecast._tcp.local. (Cache flush) [1h15m] TXT "id=f7934384-f50f-411d-8f15-dcf8ab39b5e2" "cd=f7934384-f50f-411d-8f15                                                                                                                                                              -dcf8ab39b5e2" "rm=88C28054F189A25C" "ve=05" "md=Google Cast Group" "ic=/setup/icon.png" "fn=Beneden-binnen" "ca=198692" "st=1                                                                                                                                                              " "bs=FA8FCA8D5534" "nf=1" "rs=Casting: Forever Distant" (398)
17:39:04.126406 IP (tos 0x0, ttl 255, id 52178, offset 0, flags [DF], proto UDP (17), length 394)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 3/0/0 _googlecast._tcp.local. [2m] PTR Google-Cast-Group-93d01926c                                                                                                                                                              9e04458b6bc515a347c3ecc-1._googlecast._tcp.local., Google-Cast-Group-93d01926c9e04458b6bc515a347c3ecc-1._googlecast._tcp.local                                                                                                                                                              . (Cache flush) [2m] SRV 342ddd43-4372-2cdf-d284-401f9284f6b0.local.:42539 0 0, Google-Cast-Group-93d01926c9e04458b6bc515a347c                                                                                                                                                              3ecc-1._googlecast._tcp.local. (Cache flush) [1h15m] TXT "id=93d01926-c9e0-4458-b6bc-515a347c3ecc" "cd=93d01926-c9e0-4458-b6bc                                                                                                                                                              -515a347c3ecc" "rm=88C28054F189A25C" "ve=05" "md=Google Cast Group" "ic=/setup/icon.png" "fn=Binnen" "ca=198692" "st=0" "bs=FA                                                                                                                                                              8FCA8D5534" "nf=1" "rs=" (366)
17:39:04.132540 IP (tos 0x0, ttl 255, id 52179, offset 0, flags [DF], proto UDP (17), length 395)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 3/0/0 _googlecast._tcp.local. [2m] PTR Google-Cast-Group-e63b80d72                                                                                                                                                              8e44ebf9ba30ce60e73e8ff-1._googlecast._tcp.local., Google-Cast-Group-e63b80d728e44ebf9ba30ce60e73e8ff-1._googlecast._tcp.local                                                                                                                                                              . (Cache flush) [2m] SRV 342ddd43-4372-2cdf-d284-401f9284f6b0.local.:42008 0 0, Google-Cast-Group-e63b80d728e44ebf9ba30ce60e73                                                                                                                                                              e8ff-1._googlecast._tcp.local. (Cache flush) [1h15m] TXT "id=e63b80d7-28e4-4ebf-9ba3-0ce60e73e8ff" "cd=e63b80d7-28e4-4ebf-9ba3                                                                                                                                                              -0ce60e73e8ff" "rm=88C28054F189A25C" "ve=05" "md=Google Cast Group" "ic=/setup/icon.png" "fn=Beneden" "ca=198692" "st=0" "bs=F                                                                                                                                                              A8FCA8D5534" "nf=1" "rs=" (367)
17:39:04.172967 IP (tos 0x0, ttl 255, id 52180, offset 0, flags [DF], proto UDP (17), length 68)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0 PTR (QM)? _googlecast._tcp.local. (40)
17:39:04.175666 IP (tos 0x0, ttl 255, id 52181, offset 0, flags [DF], proto UDP (17), length 118)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0 SRV (QM)? google-nest-mini-3777e026f00151e250f0cf3c65a3883d._googlecast._                                                                                                                                                              tcp.local. (90)
17:39:04.181402 IP (tos 0x0, ttl 255, id 52182, offset 0, flags [DF], proto UDP (17), length 407)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 4/0/0 _googlecast._tcp.local. [2m] PTR Google-Nest-Mini-3777e026f0                                                                                                                                                              0151e250f0cf3c65a3883d._googlecast._tcp.local., 3777e026-f001-51e2-50f0-cf3c65a3883d.local. (Cache flush) [2m] A 172.17.114.27                                                                                                                                                              , Google-Nest-Mini-3777e026f00151e250f0cf3c65a3883d._googlecast._tcp.local. (Cache flush) [2m] SRV 3777e026-f001-51e2-50f0-cf3                                                                                                                                                              c65a3883d.local.:8009 0 0, Google-Nest-Mini-3777e026f00151e250f0cf3c65a3883d._googlecast._tcp.local. (Cache flush) [1h15m] TXT                                                                                                                                                               "id=3777e026f00151e250f0cf3c65a3883d" "cd=DFE00222F401A69E6326485C9B3A7082" "rm=A333E9E22123C646" "ve=05" "md=Google Nest Min                                                                                                                                                              i" "ic=/setup/icon.png" "fn=Veranda speaker" "ca=198660" "st=0" "bs=FA8FCA3BC57B" "nf=1" "rs=" (379)
17:39:04.195717 IP (tos 0x0, ttl 255, id 52183, offset 0, flags [DF], proto UDP (17), length 121)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0 SRV (QM)? google-cast-group-f7934384f50f411d8f15dcf8ab39b5e2-1._googlecas                                                                                                                                                              t._tcp.local. (93)
17:39:04.200031 IP (tos 0x0, ttl 255, id 52184, offset 0, flags [DF], proto UDP (17), length 121)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0 SRV (QM)? google-cast-group-93d01926c9e04458b6bc515a347c3ecc-1._googlecas                                                                                                                                                              t._tcp.local. (93)
17:39:04.230735 IP (tos 0x0, ttl 255, id 52187, offset 0, flags [DF], proto UDP (17), length 422)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 4/0/0 _googlecast._tcp.local. [2m] PTR Google-Nest-Mini-7ae811b761                                                                                                                                                              f23416eca5883a6a1d18fb._googlecast._tcp.local., 7ae811b7-61f2-3416-eca5-883a6a1d18fb.local. (Cache flush) [2m] A 172.17.114.52                                                                                                                                                              , Google-Nest-Mini-7ae811b761f23416eca5883a6a1d18fb._googlecast._tcp.local. (Cache flush) [2m] SRV 7ae811b7-61f2-3416-eca5-883                                                                                                                                                              a6a1d18fb.local.:8009 0 0, Google-Nest-Mini-7ae811b761f23416eca5883a6a1d18fb._googlecast._tcp.local. (Cache flush) [1h15m] TXT                                                                                                                                                               "id=7ae811b761f23416eca5883a6a1d18fb" "cd=85A57C757FBEACA4A8C5539E4D17F49E" "rm=64F4C69BBE0D2630" "ve=05" "md=Google Nest Min                                                                                                                                                              i" "ic=/setup/icon.png" "fn=Keuken" "ca=198660" "st=1" "bs=FA8FCA6EB8E5" "nf=1" "rs=Casting: Forever Distant" (394)
17:39:04.235218 IP (tos 0x0, ttl 255, id 52188, offset 0, flags [DF], proto UDP (17), length 121)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0 SRV (QM)? google-cast-group-e63b80d728e44ebf9ba30ce60e73e8ff-1._googlecas                                                                                                                                                              t._tcp.local. (93)
17:39:04.361020 IP (tos 0x0, ttl 255, id 52198, offset 0, flags [DF], proto UDP (17), length 67)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0 PTR (QM)? _googlerpc._tcp.local. (39)
17:39:04.363771 IP (tos 0x0, ttl 255, id 52199, offset 0, flags [DF], proto UDP (17), length 79)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0 SRV (QM)? googlerpc-2._googlerpc._tcp.local. (51)
17:39:04.368776 IP (tos 0x0, ttl 255, id 52200, offset 0, flags [DF], proto UDP (17), length 192)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 3/0/0 _googlerpc._tcp.local. [2m] PTR googlerpc-2._googlerpc._tcp.                                                                                                                                                              local., googlerpc-2._googlerpc._tcp.local. (Cache flush) [2m] SRV e8b58877-627a-8cea-281b-68f6f4a17d69.local.:8012 0 0, google                                                                                                                                                              rpc-2._googlerpc._tcp.local. (Cache flush) [1h15m] TXT "cd=C4D26B8C90E081C1D8DB77EB7294BDA9" (164)
17:39:04.389617 IP (tos 0x0, ttl 255, id 52202, offset 0, flags [DF], proto UDP (17), length 192)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 3/0/0 _googlerpc._tcp.local. [2m] PTR googlerpc-1._googlerpc._tcp.                                                                                                                                                              local., googlerpc-1._googlerpc._tcp.local. (Cache flush) [2m] SRV 5fd01e95-241c-a3d6-277f-62eb6326b954.local.:8012 0 0, google                                                                                                                                                              rpc-1._googlerpc._tcp.local. (Cache flush) [1h15m] TXT "cd=6B0130740790B7044ED2EA5C3CB07A7B" (164)
17:39:04.413024 IP (tos 0x0, ttl 255, id 52203, offset 0, flags [DF], proto UDP (17), length 192)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 3/0/0 _googlerpc._tcp.local. [2m] PTR googlerpc-3._googlerpc._tcp.                                                                                                                                                              local., googlerpc-3._googlerpc._tcp.local. (Cache flush) [2m] SRV 3777e026-f001-51e2-50f0-cf3c65a3883d.local.:8012 0 0, google                                                                                                                                                              rpc-3._googlerpc._tcp.local. (Cache flush) [1h15m] TXT "cd=DFE00222F401A69E6326485C9B3A7082" (164)
17:39:04.482366 IP (tos 0x0, ttl 255, id 52207, offset 0, flags [DF], proto UDP (17), length 68)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0 PTR (QM)? _googlecast._tcp.local. (40)
17:39:04.484664 IP (tos 0x0, ttl 255, id 52208, offset 0, flags [DF], proto UDP (17), length 118)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0 SRV (QM)? google-nest-mini-7ae811b761f23416eca5883a6a1d18fb._googlecast._                                                                                                                                                              tcp.local. (90)
17:39:04.549982 IP (tos 0x0, ttl 255, id 52212, offset 0, flags [DF], proto UDP (17), length 67)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0 PTR (QM)? _googlerpc._tcp.local. (39)
17:39:04.552762 IP (tos 0x0, ttl 255, id 52213, offset 0, flags [DF], proto UDP (17), length 77)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0 SRV (QM)? googlerpc._googlerpc._tcp.local. (49)
17:39:04.559447 IP (tos 0x0, ttl 255, id 52214, offset 0, flags [DF], proto UDP (17), length 190)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 3/0/0 _googlerpc._tcp.local. [2m] PTR googlerpc._googlerpc._tcp.lo                                                                                                                                                              cal., googlerpc._googlerpc._tcp.local. (Cache flush) [2m] SRV 7ae811b7-61f2-3416-eca5-883a6a1d18fb.local.:8012 0 0, googlerpc.                                                                                                                                                              _googlerpc._tcp.local. (Cache flush) [1h15m] TXT "cd=85A57C757FBEACA4A8C5539E4D17F49E" (162)
17:39:04.563895 IP (tos 0x0, ttl 255, id 52215, offset 0, flags [DF], proto UDP (17), length 79)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0 SRV (QM)? googlerpc-2._googlerpc._tcp.local. (51)
17:39:04.567854 IP (tos 0x0, ttl 255, id 52216, offset 0, flags [DF], proto UDP (17), length 79)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0 SRV (QM)? googlerpc-3._googlerpc._tcp.local. (51)
17:39:04.575543 IP (tos 0x0, ttl 255, id 52217, offset 0, flags [DF], proto UDP (17), length 79)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0 SRV (QM)? googlerpc-1._googlerpc._tcp.local. (51)
17:39:04.626593 IP (tos 0x0, ttl 255, id 52221, offset 0, flags [DF], proto UDP (17), length 426)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 3/0/0 _googlecast._tcp.local. [2m] PTR Google-Cast-Group-f7934384f                                                                                                                                                              50f411d8f15dcf8ab39b5e2-1._googlecast._tcp.local., Google-Cast-Group-f7934384f50f411d8f15dcf8ab39b5e2-1._googlecast._tcp.local                                                                                                                                                              . (Cache flush) [2m] SRV 342ddd43-4372-2cdf-d284-401f9284f6b0.local.:32901 0 0, Google-Cast-Group-f7934384f50f411d8f15dcf8ab39                                                                                                                                                              b5e2-1._googlecast._tcp.local. (Cache flush) [1h15m] TXT "id=f7934384-f50f-411d-8f15-dcf8ab39b5e2" "cd=f7934384-f50f-411d-8f15                                                                                                                                                              -dcf8ab39b5e2" "rm=88C28054F189A25C" "ve=05" "md=Google Cast Group" "ic=/setup/icon.png" "fn=Beneden-binnen" "ca=198692" "st=1                                                                                                                                                              " "bs=FA8FCA8D5534" "nf=1" "rs=Casting: Forever Distant" (398)
17:39:04.633756 IP (tos 0x0, ttl 255, id 52222, offset 0, flags [DF], proto UDP (17), length 394)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 3/0/0 _googlecast._tcp.local. [2m] PTR Google-Cast-Group-93d01926c                                                                                                                                                              9e04458b6bc515a347c3ecc-1._googlecast._tcp.local., Google-Cast-Group-93d01926c9e04458b6bc515a347c3ecc-1._googlecast._tcp.local                                                                                                                                                              . (Cache flush) [2m] SRV 342ddd43-4372-2cdf-d284-401f9284f6b0.local.:42539 0 0, Google-Cast-Group-93d01926c9e04458b6bc515a347c                                                                                                                                                              3ecc-1._googlecast._tcp.local. (Cache flush) [1h15m] TXT "id=93d01926-c9e0-4458-b6bc-515a347c3ecc" "cd=93d01926-c9e0-4458-b6bc                                                                                                                                                              -515a347c3ecc" "rm=88C28054F189A25C" "ve=05" "md=Google Cast Group" "ic=/setup/icon.png" "fn=Binnen" "ca=198692" "st=0" "bs=FA                                                                                                                                                              8FCA8D5534" "nf=1" "rs=" (366)
17:39:04.639554 IP (tos 0x0, ttl 255, id 52223, offset 0, flags [DF], proto UDP (17), length 395)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 3/0/0 _googlecast._tcp.local. [2m] PTR Google-Cast-Group-e63b80d72                                                                                                                                                              8e44ebf9ba30ce60e73e8ff-1._googlecast._tcp.local., Google-Cast-Group-e63b80d728e44ebf9ba30ce60e73e8ff-1._googlecast._tcp.local                                                                                                                                                              . (Cache flush) [2m] SRV 342ddd43-4372-2cdf-d284-401f9284f6b0.local.:42008 0 0, Google-Cast-Group-e63b80d728e44ebf9ba30ce60e73                                                                                                                                                              e8ff-1._googlecast._tcp.local. (Cache flush) [1h15m] TXT "id=e63b80d7-28e4-4ebf-9ba3-0ce60e73e8ff" "cd=e63b80d7-28e4-4ebf-9ba3                                                                                                                                                              -0ce60e73e8ff" "rm=88C28054F189A25C" "ve=05" "md=Google Cast Group" "ic=/setup/icon.png" "fn=Beneden" "ca=198692" "st=0" "bs=F                                                                                                                                                              A8FCA8D5534" "nf=1" "rs=" (367)
17:39:04.648302 IP (tos 0x0, ttl 255, id 52224, offset 0, flags [DF], proto UDP (17), length 398)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 4/0/0 _googlecast._tcp.local. [2m] PTR Google-Nest-Mini-e8b5887762                                                                                                                                                              7a8cea281b68f6f4a17d69._googlecast._tcp.local., e8b58877-627a-8cea-281b-68f6f4a17d69.local. (Cache flush) [2m] A 172.17.114.31                                                                                                                                                              , Google-Nest-Mini-e8b58877627a8cea281b68f6f4a17d69._googlecast._tcp.local. (Cache flush) [2m] SRV e8b58877-627a-8cea-281b-68f                                                                                                                                                              6f4a17d69.local.:8009 0 0, Google-Nest-Mini-e8b58877627a8cea281b68f6f4a17d69._googlecast._tcp.local. (Cache flush) [1h15m] TXT                                                                                                                                                               "id=e8b58877627a8cea281b68f6f4a17d69" "cd=C4D26B8C90E081C1D8DB77EB7294BDA9" "rm=6A07C12CBEA61E31" "ve=05" "md=Google Nest Min                                                                                                                                                              i" "ic=/setup/icon.png" "fn=Zolder" "ca=198660" "st=0" "bs=FA8FCA706ACF" "nf=1" "rs=" (370)
17:39:13.408172 IP6 (flowlabel 0x78f70, hlim 255, next-header UDP (17) payload length: 227) fe80::f29f:c2ff:fe17:704c.5353 > f                                                                                                                                                              f02::fb.5353: [udp sum ok] 0*- [0q] 6/0/0 53.114.17.172.in-addr.arpa. (Cache flush) [2m] PTR Android.local., Android.local. (C                                                                                                                                                              ache flush) [2m] NSEC, 7.8.0.9.4.3.E.F.F.F.5.E.E.C.0.2.0.0.0.0.0.0.0.0.0.0.0.0.0.8.E.F.ip6.arpa. (Cache flush) [2m] NSEC, 53.1                                                                                                                                                              14.17.172.in-addr.arpa. (Cache flush) [2m] NSEC, Android.local. (Cache flush) [2m] A 172.17.114.53, 7.8.0.9.4.3.E.F.F.F.5.E.E.                                                                                                                                                              C.0.2.0.0.0.0.0.0.0.0.0.0.0.0.0.8.E.F.ip6.arpa. (Cache flush) [2m] PTR Android.local. (219)
17:39:50.270450 IP (tos 0x0, ttl 255, id 54288, offset 0, flags [DF], proto UDP (17), length 73)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0 PTR (QM)? _spotify-connect._tcp.local. (45)
17:39:52.331182 IP (tos 0x0, ttl 128, id 1, offset 0, flags [DF], proto UDP (17), length 328)
    0.0.0.0.68 > 255.255.255.255.67: [udp sum ok] BOOTP/DHCP, Request from 58:d5:0a:b3:6b:e1, length 300, xid 0xab3f54e, Flags                                                                                                                                                               [Broadcast] (0x8000)
          Client-Ethernet-Address 58:d5:0a:b3:6b:e1
          Vendor-rfc1048 Extensions
            Magic Cookie 0x63825363
            DHCP-Message Option 53, length 1: Discover
            Lease-Time Option 51, length 4: 4294967295
            Hostname Option 12, length 15: "GW-58D50AB36BE1"
            Parameter-Request Option 55, length 3:
              Subnet-Mask, Default-Gateway, Domain-Name-Server
            END Option 255, length 0
            PAD Option 0, length 0, occurs 28
17:39:52.332220 ARP, Ethernet (len 6), IPv4 (len 4), Request who-has 10.1.0.18 tell 10.1.0.1, length 28
17:39:53.332875 IP (tos 0x10, ttl 128, id 0, offset 0, flags [none], proto UDP (17), length 328)
    10.1.0.1.67 > 255.255.255.255.68: [udp sum ok] BOOTP/DHCP, Reply, length 300, xid 0xab3f54e, Flags [Broadcast] (0x8000)
          Your-IP 10.1.0.18
          Client-Ethernet-Address 58:d5:0a:b3:6b:e1
          Vendor-rfc1048 Extensions
            Magic Cookie 0x63825363
            DHCP-Message Option 53, length 1: Offer
            Server-ID Option 54, length 4: 10.1.0.1
            Lease-Time Option 51, length 4: 86400
            Subnet-Mask Option 1, length 4: 255.255.0.0
            Default-Gateway Option 3, length 4: 10.1.0.1
            Domain-Name-Server Option 6, length 4: 10.1.0.1
            END Option 255, length 0
            PAD Option 0, length 0, occurs 26
17:39:53.333086 IP (tos 0x0, ttl 128, id 2, offset 0, flags [DF], proto UDP (17), length 328)
    0.0.0.0.68 > 255.255.255.255.67: [udp sum ok] BOOTP/DHCP, Request from 58:d5:0a:b3:6b:e1, length 300, xid 0xab3f54e, secs                                                                                                                                                               1, Flags [Broadcast] (0x8000)
          Client-Ethernet-Address 58:d5:0a:b3:6b:e1
          Vendor-rfc1048 Extensions
            Magic Cookie 0x63825363
            DHCP-Message Option 53, length 1: Request
            Hostname Option 12, length 15: "GW-58D50AB36BE1"
            Requested-IP Option 50, length 4: 10.1.0.18
            Server-ID Option 54, length 4: 10.1.0.1
            Parameter-Request Option 55, length 3:
              Subnet-Mask, Default-Gateway, Domain-Name-Server
            END Option 255, length 0
            PAD Option 0, length 0, occurs 22
17:39:53.337109 IP (tos 0x10, ttl 128, id 0, offset 0, flags [none], proto UDP (17), length 328)
    10.1.0.1.67 > 255.255.255.255.68: [udp sum ok] BOOTP/DHCP, Reply, length 300, xid 0xab3f54e, secs 1, Flags [Broadcast] (0x                                                                                                                                                              8000)
          Your-IP 10.1.0.18
          Client-Ethernet-Address 58:d5:0a:b3:6b:e1
          Vendor-rfc1048 Extensions
            Magic Cookie 0x63825363
            DHCP-Message Option 53, length 1: ACK
            Server-ID Option 54, length 4: 10.1.0.1
            Lease-Time Option 51, length 4: 86400
            Subnet-Mask Option 1, length 4: 255.255.0.0
            Default-Gateway Option 3, length 4: 10.1.0.1
            Domain-Name-Server Option 6, length 4: 10.1.0.1
            END Option 255, length 0
            PAD Option 0, length 0, occurs 26
17:39:53.400293 ARP, Ethernet (len 6), IPv4 (len 4), Request who-has 10.1.0.18 tell 10.1.0.1, length 28
17:39:54.331124 ARP, Ethernet (len 6), IPv4 (len 4), Request who-has 10.1.0.18 tell 0.0.0.0, length 46
17:39:54.440288 ARP, Ethernet (len 6), IPv4 (len 4), Request who-has 10.1.0.18 tell 10.1.0.1, length 28
17:39:55.331121 ARP, Ethernet (len 6), IPv4 (len 4), Request who-has 10.1.0.18 tell 0.0.0.0, length 46
17:39:57.331169 ARP, Ethernet (len 6), IPv4 (len 4), Request who-has 10.1.0.18 tell 0.0.0.0, length 46
17:39:57.429124 IP6 (hlim 255, next-header ICMPv6 (58) payload length: 24) :: > ff02::1:ffb3:6be1: [icmp6 sum ok] ICMP6, neigh                                                                                                                                                              bor solicitation, length 24, who has fe80::5ad5:aff:feb3:6be1
17:39:58.329121 IP6 (hlim 255, next-header ICMPv6 (58) payload length: 24) :: > ff02::1:ffb3:6be1: [icmp6 sum ok] ICMP6, neigh                                                                                                                                                              bor solicitation, length 24, who has fe80::5ad5:aff:feb3:6be1
17:39:59.329121 IP6 (hlim 255, next-header ICMPv6 (58) payload length: 24) :: > ff02::1:ffb3:6be1: [icmp6 sum ok] ICMP6, neigh                                                                                                                                                              bor solicitation, length 24, who has fe80::5ad5:aff:feb3:6be1
17:39:59.497842 IP (tos 0x0, ttl 255, id 54856, offset 0, flags [DF], proto UDP (17), length 206)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 4/0/0 _googlerpc._tcp.local. [2m] PTR googlerpc._googlerpc._tcp.lo                                                                                                                                                              cal., 7ae811b7-61f2-3416-eca5-883a6a1d18fb.local. (Cache flush) [2m] A 172.17.114.52, googlerpc._googlerpc._tcp.local. (Cache                                                                                                                                                               flush) [2m] SRV 7ae811b7-61f2-3416-eca5-883a6a1d18fb.local.:8012 0 0, googlerpc._googlerpc._tcp.local. (Cache flush) [1h15m] T                                                                                                                                                              XT "cd=85A57C757FBEACA4A8C5539E4D17F49E" (178)
17:39:59.503058 IP (tos 0x0, ttl 255, id 54857, offset 0, flags [DF], proto UDP (17), length 399)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 3/0/0 _googlecast._tcp.local. [2m] PTR Google-Nest-Mini-7ae811b761                                                                                                                                                              f23416eca5883a6a1d18fb._googlecast._tcp.local., Google-Nest-Mini-7ae811b761f23416eca5883a6a1d18fb._googlecast._tcp.local. (Cac                                                                                                                                                              he flush) [2m] SRV 7ae811b7-61f2-3416-eca5-883a6a1d18fb.local.:8009 0 0, Google-Nest-Mini-7ae811b761f23416eca5883a6a1d18fb._go                                                                                                                                                              oglecast._tcp.local. (Cache flush) [1h15m] TXT "id=7ae811b761f23416eca5883a6a1d18fb" "cd=85A57C757FBEACA4A8C5539E4D17F49E" "rm                                                                                                                                                              =64F4C69BBE0D2630" "ve=05" "md=Google Nest Mini" "ic=/setup/icon.png" "fn=Keuken" "ca=198660" "st=1" "bs=FA8FCA6EB8E5" "nf=1"                                                                                                                                                               "rs=Casting: Drifting" (371)
17:39:59.509487 IP (tos 0x0, ttl 255, id 54858, offset 0, flags [DF], proto UDP (17), length 285)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 3/0/0 _%%F6934AFB-9DEB-4740-A2EC-9DAF4EBDEA3F._sub._googlecast._tc                                                                                                                                                              p.local. [2m] PTR Google-Nest-Mini-7ae811b761f23416eca5883a6a1d18fb._googlecast._tcp.local., _%9E5E7C8F47989526C9BCD95D24084F6                                                                                                                                                              F0B27C5ED._sub._googlecast._tcp.local. [2m] PTR Google-Nest-Mini-7ae811b761f23416eca5883a6a1d18fb._googlecast._tcp.local., _%6                                                                                                                                                              DB85AEB67287F47BA7D2A1B36F88DB848080920._sub._googlecast._tcp.local. [2m] PTR Google-Nest-Mini-7ae811b761f23416eca5883a6a1d18f                                                                                                                                                              b._googlecast._tcp.local. (257)
17:39:59.515889 IP (tos 0x0, ttl 255, id 54859, offset 0, flags [DF], proto UDP (17), length 385)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 3/0/0 _googlezone._tcp.local. [2m] PTR 7ae811b7-61f2-3416-eca5-883                                                                                                                                                              a6a1d18fb._googlezone._tcp.local., 7ae811b7-61f2-3416-eca5-883a6a1d18fb._googlezone._tcp.local. (Cache flush) [2m] SRV 7ae811b                                                                                                                                                              7-61f2-3416-eca5-883a6a1d18fb.local.:10001 610 3, 7ae811b7-61f2-3416-eca5-883a6a1d18fb._googlezone._tcp.local. (Cache flush) [                                                                                                                                                              1h15m] TXT "id=85A57C757FBEACA4A8C5539E4D17F49E" "93d01926-c9e0-4458-b6bc-515a347c3ecc=0|Binnen" "e63b80d7-28e4-4ebf-9ba3-0ce6                                                                                                                                                              0e73e8ff=0|Beneden" "f7934384-f50f-411d-8f15-dcf8ab39b5e2=0|Beneden-binnen" "__common_time__=0|0" (357)
17:39:59.523004 IP (tos 0x0, ttl 255, id 54860, offset 0, flags [DF], proto UDP (17), length 401)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 4/0/0 _googlezone._tcp.local. [2m] PTR 342ddd43-4372-2cdf-d284-401                                                                                                                                                              f9284f6b0._googlezone._tcp.local., 342ddd43-4372-2cdf-d284-401f9284f6b0.local. (Cache flush) [2m] A 172.17.114.18, 342ddd43-43                                                                                                                                                              72-2cdf-d284-401f9284f6b0._googlezone._tcp.local. (Cache flush) [2m] SRV 342ddd43-4372-2cdf-d284-401f9284f6b0.local.:10001 610                                                                                                                                                               123, 342ddd43-4372-2cdf-d284-401f9284f6b0._googlezone._tcp.local. (Cache flush) [1h15m] TXT "id=D44812348A098CDF225570FC4FBA7                                                                                                                                                              F1A" "93d01926-c9e0-4458-b6bc-515a347c3ecc=1|Binnen" "e63b80d7-28e4-4ebf-9ba3-0ce60e73e8ff=1|Beneden" "f7934384-f50f-411d-8f15                                                                                                                                                              -dcf8ab39b5e2=3|Beneden-binnen" "__common_time__=0|0" (373)
17:39:59.529941 IP (tos 0x0, ttl 255, id 54861, offset 0, flags [DF], proto UDP (17), length 401)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 3/0/0 _googlecast._tcp.local. [2m] PTR Chromecast-Audio-342ddd4343                                                                                                                                                              722cdfd284401f9284f6b0._googlecast._tcp.local., Chromecast-Audio-342ddd4343722cdfd284401f9284f6b0._googlecast._tcp.local. (Cac                                                                                                                                                              he flush) [2m] SRV 342ddd43-4372-2cdf-d284-401f9284f6b0.local.:8009 0 0, Chromecast-Audio-342ddd4343722cdfd284401f9284f6b0._go                                                                                                                                                              oglecast._tcp.local. (Cache flush) [1h15m] TXT "id=342ddd4343722cdfd284401f9284f6b0" "cd=D44812348A098CDF225570FC4FBA7F1A" "rm                                                                                                                                                              =88C28054F189A25C" "ve=05" "md=Chromecast Audio" "ic=/setup/icon.png" "fn=AudioPro" "ca=198660" "st=1" "bs=FA8FCA8D5534" "nf=1                                                                                                                                                              " "rs=Casting: Drifting" (373)
17:39:59.536841 IP (tos 0x0, ttl 255, id 54862, offset 0, flags [DF], proto UDP (17), length 419)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 3/0/0 _googlecast._tcp.local. [2m] PTR Google-Cast-Group-f7934384f                                                                                                                                                              50f411d8f15dcf8ab39b5e2-1._googlecast._tcp.local., Google-Cast-Group-f7934384f50f411d8f15dcf8ab39b5e2-1._googlecast._tcp.local                                                                                                                                                              . (Cache flush) [2m] SRV 342ddd43-4372-2cdf-d284-401f9284f6b0.local.:32901 0 0, Google-Cast-Group-f7934384f50f411d8f15dcf8ab39                                                                                                                                                              b5e2-1._googlecast._tcp.local. (Cache flush) [1h15m] TXT "id=f7934384-f50f-411d-8f15-dcf8ab39b5e2" "cd=f7934384-f50f-411d-8f15                                                                                                                                                              -dcf8ab39b5e2" "rm=88C28054F189A25C" "ve=05" "md=Google Cast Group" "ic=/setup/icon.png" "fn=Beneden-binnen" "ca=198692" "st=1                                                                                                                                                              " "bs=FA8FCA8D5534" "nf=1" "rs=Casting: Drifting" (391)
17:39:59.549345 IP (tos 0x0, ttl 255, id 54863, offset 0, flags [DF], proto UDP (17), length 573)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 8/0/0 _%%C6D649ED-C3A2-45CD-B8B8-99F868FA6028._sub._googlecast._tc                                                                                                                                                              p.local. [2m] PTR Google-Cast-Group-f7934384f50f411d8f15dcf8ab39b5e2-1._googlecast._tcp.local., _%CFD711A95AA6B74712716F312683                                                                                                                                                              F658BA76AFA7._sub._googlecast._tcp.local. [2m] PTR Google-Cast-Group-f7934384f50f411d8f15dcf8ab39b5e2-1._googlecast._tcp.local                                                                                                                                                              ., _%C16B29D865E2B377DBA1D0B81D89E4BDF62AF162._sub._googlecast._tcp.local. [2m] PTR Google-Cast-Group-f7934384f50f411d8f15dcf8                                                                                                                                                              ab39b5e2-1._googlecast._tcp.local., _%9E5E7C8F47989526C9BCD95D24084F6F0B27C5ED._sub._googlecast._tcp.local. [2m] PTR Google-Ca                                                                                                                                                              st-Group-f7934384f50f411d8f15dcf8ab39b5e2-1._googlecast._tcp.local., _%6DB85AEB67287F47BA7D2A1B36F88DB848080920._sub._googleca                                                                                                                                                              st._tcp.local. [2m] PTR Google-Cast-Group-f7934384f50f411d8f15dcf8ab39b5e2-1._googlecast._tcp.local., _%65623D10A96E95064450CE                                                                                                                                                              BF43B3CFE5BA14A1DC._sub._googlecast._tcp.local. [2m] PTR Google-Cast-Group-f7934384f50f411d8f15dcf8ab39b5e2-1._googlecast._tcp                                                                                                                                                              .local., _%3B80215ECB8EF438A1BB3E28D11D42C04A4013CE._sub._googlecast._tcp.local. [2m] PTR Google-Cast-Group-f7934384f50f411d8f                                                                                                                                                              15dcf8ab39b5e2-1._googlecast._tcp.local., _%390BFA306A07693043161F476B5C37844A28FB68._sub._googlecast._tcp.local. [2m] PTR Goo                                                                                                                                                              gle-Cast-Group-f7934384f50f411d8f15dcf8ab39b5e2-1._googlecast._tcp.local. (545)
17:39:59.554843 IP (tos 0x0, ttl 255, id 54864, offset 0, flags [DF], proto UDP (17), length 394)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 3/0/0 _googlecast._tcp.local. [2m] PTR Google-Cast-Group-93d01926c                                                                                                                                                              9e04458b6bc515a347c3ecc-1._googlecast._tcp.local., Google-Cast-Group-93d01926c9e04458b6bc515a347c3ecc-1._googlecast._tcp.local                                                                                                                                                              . (Cache flush) [2m] SRV 342ddd43-4372-2cdf-d284-401f9284f6b0.local.:42539 0 0, Google-Cast-Group-93d01926c9e04458b6bc515a347c                                                                                                                                                              3ecc-1._googlecast._tcp.local. (Cache flush) [1h15m] TXT "id=93d01926-c9e0-4458-b6bc-515a347c3ecc" "cd=93d01926-c9e0-4458-b6bc                                                                                                                                                              -515a347c3ecc" "rm=88C28054F189A25C" "ve=05" "md=Google Cast Group" "ic=/setup/icon.png" "fn=Binnen" "ca=198692" "st=0" "bs=FA                                                                                                                                                              8FCA8D5534" "nf=1" "rs=" (366)
17:39:59.559791 IP (tos 0x0, ttl 255, id 54865, offset 0, flags [DF], proto UDP (17), length 395)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 3/0/0 _googlecast._tcp.local. [2m] PTR Google-Cast-Group-e63b80d72                                                                                                                                                              8e44ebf9ba30ce60e73e8ff-1._googlecast._tcp.local., Google-Cast-Group-e63b80d728e44ebf9ba30ce60e73e8ff-1._googlecast._tcp.local                                                                                                                                                              . (Cache flush) [2m] SRV 342ddd43-4372-2cdf-d284-401f9284f6b0.local.:42008 0 0, Google-Cast-Group-e63b80d728e44ebf9ba30ce60e73                                                                                                                                                              e8ff-1._googlecast._tcp.local. (Cache flush) [1h15m] TXT "id=e63b80d7-28e4-4ebf-9ba3-0ce60e73e8ff" "cd=e63b80d7-28e4-4ebf-9ba3                                                                                                                                                              -0ce60e73e8ff" "rm=88C28054F189A25C" "ve=05" "md=Google Cast Group" "ic=/setup/icon.png" "fn=Beneden" "ca=198692" "st=0" "bs=F                                                                                                                                                              A8FCA8D5534" "nf=1" "rs=" (367)
17:40:00.431139 IP6 (hlim 255, next-header UDP (17) payload length: 110) fe80::5ad5:aff:feb3:6be1.5353 > ff02::fb.5353: [udp s                                                                                                                                                              um ok] 0 [1n] ANY (QM)? TRADFRI-Gateway-58d50ab36be1.local. ns: TRADFRI-Gateway-58d50ab36be1.local. [2m] A 10.1.0.18 (102)
17:40:00.431306 IP (tos 0x0, ttl 255, id 3, offset 0, flags [DF], proto UDP (17), length 130)
    10.1.0.18.5353 > 224.0.0.251.5353: [udp sum ok] 0 [1n] ANY (QM)? TRADFRI-Gateway-58d50ab36be1.local. ns: TRADFRI-Gateway-5                                                                                                                                                              8d50ab36be1.local. [2m] A 10.1.0.18 (102)
17:40:00.500433 IP (tos 0x0, ttl 255, id 54877, offset 0, flags [DF], proto UDP (17), length 206)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 4/0/0 _googlerpc._tcp.local. [2m] PTR googlerpc._googlerpc._tcp.lo                                                                                                                                                              cal., 7ae811b7-61f2-3416-eca5-883a6a1d18fb.local. (Cache flush) [2m] A 172.17.114.52, googlerpc._googlerpc._tcp.local. (Cache                                                                                                                                                               flush) [2m] SRV 7ae811b7-61f2-3416-eca5-883a6a1d18fb.local.:8012 0 0, googlerpc._googlerpc._tcp.local. (Cache flush) [1h15m] T                                                                                                                                                              XT "cd=85A57C757FBEACA4A8C5539E4D17F49E" (178)
17:40:00.503050 IP (tos 0x0, ttl 255, id 54878, offset 0, flags [DF], proto UDP (17), length 399)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 3/0/0 _googlecast._tcp.local. [2m] PTR Google-Nest-Mini-7ae811b761                                                                                                                                                              f23416eca5883a6a1d18fb._googlecast._tcp.local., Google-Nest-Mini-7ae811b761f23416eca5883a6a1d18fb._googlecast._tcp.local. (Cac                                                                                                                                                              he flush) [2m] SRV 7ae811b7-61f2-3416-eca5-883a6a1d18fb.local.:8009 0 0, Google-Nest-Mini-7ae811b761f23416eca5883a6a1d18fb._go                                                                                                                                                              oglecast._tcp.local. (Cache flush) [1h15m] TXT "id=7ae811b761f23416eca5883a6a1d18fb" "cd=85A57C757FBEACA4A8C5539E4D17F49E" "rm                                                                                                                                                              =64F4C69BBE0D2630" "ve=05" "md=Google Nest Mini" "ic=/setup/icon.png" "fn=Keuken" "ca=198660" "st=1" "bs=FA8FCA6EB8E5" "nf=1"                                                                                                                                                               "rs=Casting: Drifting" (371)
17:40:00.506106 IP (tos 0x0, ttl 255, id 54879, offset 0, flags [DF], proto UDP (17), length 285)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 3/0/0 _%%F6934AFB-9DEB-4740-A2EC-9DAF4EBDEA3F._sub._googlecast._tc                                                                                                                                                              p.local. [2m] PTR Google-Nest-Mini-7ae811b761f23416eca5883a6a1d18fb._googlecast._tcp.local., _%9E5E7C8F47989526C9BCD95D24084F6                                                                                                                                                              F0B27C5ED._sub._googlecast._tcp.local. [2m] PTR Google-Nest-Mini-7ae811b761f23416eca5883a6a1d18fb._googlecast._tcp.local., _%6                                                                                                                                                              DB85AEB67287F47BA7D2A1B36F88DB848080920._sub._googlecast._tcp.local. [2m] PTR Google-Nest-Mini-7ae811b761f23416eca5883a6a1d18f                                                                                                                                                              b._googlecast._tcp.local. (257)
17:40:00.509171 IP (tos 0x0, ttl 255, id 54880, offset 0, flags [DF], proto UDP (17), length 385)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 3/0/0 _googlezone._tcp.local. [2m] PTR 7ae811b7-61f2-3416-eca5-883                                                                                                                                                              a6a1d18fb._googlezone._tcp.local., 7ae811b7-61f2-3416-eca5-883a6a1d18fb._googlezone._tcp.local. (Cache flush) [2m] SRV 7ae811b                                                                                                                                                              7-61f2-3416-eca5-883a6a1d18fb.local.:10001 610 3, 7ae811b7-61f2-3416-eca5-883a6a1d18fb._googlezone._tcp.local. (Cache flush) [                                                                                                                                                              1h15m] TXT "id=85A57C757FBEACA4A8C5539E4D17F49E" "93d01926-c9e0-4458-b6bc-515a347c3ecc=0|Binnen" "e63b80d7-28e4-4ebf-9ba3-0ce6                                                                                                                                                              0e73e8ff=0|Beneden" "f7934384-f50f-411d-8f15-dcf8ab39b5e2=0|Beneden-binnen" "__common_time__=0|0" (357)
17:40:00.518682 IP (tos 0x0, ttl 255, id 54881, offset 0, flags [DF], proto UDP (17), length 401)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 4/0/0 _googlezone._tcp.local. [2m] PTR 342ddd43-4372-2cdf-d284-401                                                                                                                                                              f9284f6b0._googlezone._tcp.local., 342ddd43-4372-2cdf-d284-401f9284f6b0.local. (Cache flush) [2m] A 172.17.114.18, 342ddd43-43                                                                                                                                                              72-2cdf-d284-401f9284f6b0._googlezone._tcp.local. (Cache flush) [2m] SRV 342ddd43-4372-2cdf-d284-401f9284f6b0.local.:10001 610                                                                                                                                                               123, 342ddd43-4372-2cdf-d284-401f9284f6b0._googlezone._tcp.local. (Cache flush) [1h15m] TXT "id=D44812348A098CDF225570FC4FBA7                                                                                                                                                              F1A" "93d01926-c9e0-4458-b6bc-515a347c3ecc=1|Binnen" "e63b80d7-28e4-4ebf-9ba3-0ce60e73e8ff=1|Beneden" "f7934384-f50f-411d-8f15                                                                                                                                                              -dcf8ab39b5e2=3|Beneden-binnen" "__common_time__=0|0" (373)
17:40:00.522234 IP (tos 0x0, ttl 255, id 54882, offset 0, flags [DF], proto UDP (17), length 401)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 3/0/0 _googlecast._tcp.local. [2m] PTR Chromecast-Audio-342ddd4343                                                                                                                                                              722cdfd284401f9284f6b0._googlecast._tcp.local., Chromecast-Audio-342ddd4343722cdfd284401f9284f6b0._googlecast._tcp.local. (Cac                                                                                                                                                              he flush) [2m] SRV 342ddd43-4372-2cdf-d284-401f9284f6b0.local.:8009 0 0, Chromecast-Audio-342ddd4343722cdfd284401f9284f6b0._go                                                                                                                                                              oglecast._tcp.local. (Cache flush) [1h15m] TXT "id=342ddd4343722cdfd284401f9284f6b0" "cd=D44812348A098CDF225570FC4FBA7F1A" "rm                                                                                                                                                              =88C28054F189A25C" "ve=05" "md=Chromecast Audio" "ic=/setup/icon.png" "fn=AudioPro" "ca=198660" "st=1" "bs=FA8FCA8D5534" "nf=1                                                                                                                                                              " "rs=Casting: Drifting" (373)
17:40:00.525882 IP (tos 0x0, ttl 255, id 54883, offset 0, flags [DF], proto UDP (17), length 419)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 3/0/0 _googlecast._tcp.local. [2m] PTR Google-Cast-Group-f7934384f                                                                                                                                                              50f411d8f15dcf8ab39b5e2-1._googlecast._tcp.local., Google-Cast-Group-f7934384f50f411d8f15dcf8ab39b5e2-1._googlecast._tcp.local                                                                                                                                                              . (Cache flush) [2m] SRV 342ddd43-4372-2cdf-d284-401f9284f6b0.local.:32901 0 0, Google-Cast-Group-f7934384f50f411d8f15dcf8ab39                                                                                                                                                              b5e2-1._googlecast._tcp.local. (Cache flush) [1h15m] TXT "id=f7934384-f50f-411d-8f15-dcf8ab39b5e2" "cd=f7934384-f50f-411d-8f15                                                                                                                                                              -dcf8ab39b5e2" "rm=88C28054F189A25C" "ve=05" "md=Google Cast Group" "ic=/setup/icon.png" "fn=Beneden-binnen" "ca=198692" "st=1                                                                                                                                                              " "bs=FA8FCA8D5534" "nf=1" "rs=Casting: Drifting" (391)
17:40:00.534326 IP (tos 0x0, ttl 255, id 54884, offset 0, flags [DF], proto UDP (17), length 573)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 8/0/0 _%%C6D649ED-C3A2-45CD-B8B8-99F868FA6028._sub._googlecast._tc                                                                                                                                                              p.local. [2m] PTR Google-Cast-Group-f7934384f50f411d8f15dcf8ab39b5e2-1._googlecast._tcp.local., _%CFD711A95AA6B74712716F312683                                                                                                                                                              F658BA76AFA7._sub._googlecast._tcp.local. [2m] PTR Google-Cast-Group-f7934384f50f411d8f15dcf8ab39b5e2-1._googlecast._tcp.local                                                                                                                                                              ., _%C16B29D865E2B377DBA1D0B81D89E4BDF62AF162._sub._googlecast._tcp.local. [2m] PTR Google-Cast-Group-f7934384f50f411d8f15dcf8                                                                                                                                                              ab39b5e2-1._googlecast._tcp.local., _%9E5E7C8F47989526C9BCD95D24084F6F0B27C5ED._sub._googlecast._tcp.local. [2m] PTR Google-Ca                                                                                                                                                              st-Group-f7934384f50f411d8f15dcf8ab39b5e2-1._googlecast._tcp.local., _%6DB85AEB67287F47BA7D2A1B36F88DB848080920._sub._googleca                                                                                                                                                              st._tcp.local. [2m] PTR Google-Cast-Group-f7934384f50f411d8f15dcf8ab39b5e2-1._googlecast._tcp.local., _%65623D10A96E95064450CE                                                                                                                                                              BF43B3CFE5BA14A1DC._sub._googlecast._tcp.local. [2m] PTR Google-Cast-Group-f7934384f50f411d8f15dcf8ab39b5e2-1._googlecast._tcp                                                                                                                                                              .local., _%3B80215ECB8EF438A1BB3E28D11D42C04A4013CE._sub._googlecast._tcp.local. [2m] PTR Google-Cast-Group-f7934384f50f411d8f                                                                                                                                                              15dcf8ab39b5e2-1._googlecast._tcp.local., _%390BFA306A07693043161F476B5C37844A28FB68._sub._googlecast._tcp.local. [2m] PTR Goo                                                                                                                                                              gle-Cast-Group-f7934384f50f411d8f15dcf8ab39b5e2-1._googlecast._tcp.local. (545)
17:40:00.538920 IP (tos 0x0, ttl 255, id 54885, offset 0, flags [DF], proto UDP (17), length 394)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 3/0/0 _googlecast._tcp.local. [2m] PTR Google-Cast-Group-93d01926c                                                                                                                                                              9e04458b6bc515a347c3ecc-1._googlecast._tcp.local., Google-Cast-Group-93d01926c9e04458b6bc515a347c3ecc-1._googlecast._tcp.local                                                                                                                                                              . (Cache flush) [2m] SRV 342ddd43-4372-2cdf-d284-401f9284f6b0.local.:42539 0 0, Google-Cast-Group-93d01926c9e04458b6bc515a347c                                                                                                                                                              3ecc-1._googlecast._tcp.local. (Cache flush) [1h15m] TXT "id=93d01926-c9e0-4458-b6bc-515a347c3ecc" "cd=93d01926-c9e0-4458-b6bc                                                                                                                                                              -515a347c3ecc" "rm=88C28054F189A25C" "ve=05" "md=Google Cast Group" "ic=/setup/icon.png" "fn=Binnen" "ca=198692" "st=0" "bs=FA                                                                                                                                                              8FCA8D5534" "nf=1" "rs=" (366)
17:40:00.544109 IP (tos 0x0, ttl 255, id 54886, offset 0, flags [DF], proto UDP (17), length 395)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 3/0/0 _googlecast._tcp.local. [2m] PTR Google-Cast-Group-e63b80d72                                                                                                                                                              8e44ebf9ba30ce60e73e8ff-1._googlecast._tcp.local., Google-Cast-Group-e63b80d728e44ebf9ba30ce60e73e8ff-1._googlecast._tcp.local                                                                                                                                                              . (Cache flush) [2m] SRV 342ddd43-4372-2cdf-d284-401f9284f6b0.local.:42008 0 0, Google-Cast-Group-e63b80d728e44ebf9ba30ce60e73                                                                                                                                                              e8ff-1._googlecast._tcp.local. (Cache flush) [1h15m] TXT "id=e63b80d7-28e4-4ebf-9ba3-0ce60e73e8ff" "cd=e63b80d7-28e4-4ebf-9ba3                                                                                                                                                              -0ce60e73e8ff" "rm=88C28054F189A25C" "ve=05" "md=Google Cast Group" "ic=/setup/icon.png" "fn=Beneden" "ca=198692" "st=0" "bs=F                                                                                                                                                              A8FCA8D5534" "nf=1" "rs=" (367)
17:40:00.586583 ARP, Ethernet (len 6), IPv4 (len 4), Request who-has 10.1.0.1 tell 10.1.0.18, length 46
17:40:00.586710 ARP, Ethernet (len 6), IPv4 (len 4), Reply 10.1.0.1 is-at f0:9f:c2:17:70:4c, length 28
17:40:00.586799 IP (tos 0x0, ttl 255, id 4, offset 0, flags [DF], proto UDP (17), length 68)
    10.1.0.18.54073 > 10.1.0.1.53: [udp sum ok] 63962+ A? 1.tradfri.pool.ntp.org. (40)
17:40:00.586985 IP (tos 0x0, ttl 255, id 5, offset 0, flags [DF], proto UDP (17), length 68)
    10.1.0.18.54073 > 8.8.8.8.53: [udp sum ok] 35238+ A? 1.tradfri.pool.ntp.org. (40)
17:40:00.612737 IP (tos 0x0, ttl 64, id 54399, offset 0, flags [DF], proto UDP (17), length 132)
    10.1.0.1.53 > 10.1.0.18.54073: [udp sum ok] 63962 q: A? 1.tradfri.pool.ntp.org. 4/0/0 1.tradfri.pool.ntp.org. [2m29s] A 87                                                                                                                                                              .253.148.92, 1.tradfri.pool.ntp.org. [2m29s] A 83.98.201.134, 1.tradfri.pool.ntp.org. [2m29s] A 45.32.4.67, 1.tradfri.pool.ntp                                                                                                                                                              .org. [2m29s] A 51.15.123.168 (104)
17:40:00.612891 IP (tos 0x0, ttl 255, id 6, offset 0, flags [DF], proto UDP (17), length 76)
    10.1.0.18.123 > 87.253.148.92.123: [udp sum ok] NTPv3, length 48
        Client, Leap indicator: clock unsynchronized (192), Stratum 0 (unspecified), poll 17 (131072s), precision 0
        Root Delay: 0.000000, Root dispersion: 0.000000, Reference-ID: (unspec)
          Reference Timestamp:  0.000000000
          Originator Timestamp: 0.000000000
          Receive Timestamp:    0.000000000
          Transmit Timestamp:   2208988820.000000000 (1970/01/01 00:00:20)
            Originator - Receive Timestamp:  0.000000000
            Originator - Transmit Timestamp: 2208988820.000000000 (1970/01/01 00:00:20)
17:40:00.618715 IP (tos 0xb8, ttl 56, id 38288, offset 0, flags [DF], proto UDP (17), length 76)
    87.253.148.92.123 > 10.1.0.18.123: [udp sum ok] NTPv3, length 48
        Server, Leap indicator:  (0), Stratum 2 (secondary reference), poll 17 (131072s), precision -24
        Root Delay: 0.001174, Root dispersion: 0.018569, Reference-ID: 193.79.237.14
          Reference Timestamp:  3816956201.726410012 (2020/12/14 17:36:41)
          Originator Timestamp: 2208988820.000000000 (1970/01/01 00:00:20)
          Receive Timestamp:    3816956400.614132785 (2020/12/14 17:40:00)
          Transmit Timestamp:   3816956400.614177429 (2020/12/14 17:40:00)
            Originator - Receive Timestamp:  +1607967580.614132785
            Originator - Transmit Timestamp: +1607967580.614177429
17:40:00.644472 IP (tos 0x80, ttl 124, id 4485, offset 0, flags [none], proto UDP (17), length 132)
    8.8.8.8.53 > 10.1.0.18.54073: [udp sum ok] 35238 q: A? 1.tradfri.pool.ntp.org. 4/0/0 1.tradfri.pool.ntp.org. [2m29s] A 80.                                                                                                                                                              101.14.101, 1.tradfri.pool.ntp.org. [2m29s] A 51.15.20.83, 1.tradfri.pool.ntp.org. [2m29s] A 91.192.36.161, 1.tradfri.pool.ntp                                                                                                                                                              .org. [2m29s] A 131.211.8.244 (104)
17:40:00.644615 IP (tos 0x0, ttl 255, id 7, offset 0, flags [none], proto ICMP (1), length 56)
    10.1.0.18 > 8.8.8.8: ICMP 10.1.0.18 udp port 54073 unreachable, length 36
        IP (tos 0x80, ttl 124, id 4485, offset 0, flags [none], proto UDP (17), length 132)
    8.8.8.8.53 > 10.1.0.18.54073: [|domain]
17:40:00.931143 IP6 (hlim 255, next-header UDP (17) payload length: 110) fe80::5ad5:aff:feb3:6be1.5353 > ff02::fb.5353: [udp s                                                                                                                                                              um ok] 0 [1n] ANY (QM)? TRADFRI-Gateway-58d50ab36be1.local. ns: TRADFRI-Gateway-58d50ab36be1.local. [2m] A 10.1.0.18 (102)
17:40:00.931297 IP (tos 0x0, ttl 255, id 8, offset 0, flags [DF], proto UDP (17), length 130)
    10.1.0.18.5353 > 224.0.0.251.5353: [udp sum ok] 0 [1n] ANY (QM)? TRADFRI-Gateway-58d50ab36be1.local. ns: TRADFRI-Gateway-5                                                                                                                                                              8d50ab36be1.local. [2m] A 10.1.0.18 (102)
17:40:01.329113 IP (tos 0x0, ttl 1, id 9, offset 0, flags [none], proto IGMP (2), length 32, options (RA))
    10.1.0.18 > 224.0.0.251: igmp v2 report 224.0.0.251
17:40:01.329346 IP6 (hlim 255, next-header ICMPv6 (58) payload length: 16) fe80::5ad5:aff:feb3:6be1 > ff02::2: [icmp6 sum ok]                                                                                                                                                               ICMP6, router solicitation, length 16
          source link-address option (1), length 8 (1): 58:d5:0a:b3:6b:e1
            0x0000:  58d5 0ab3 6be1
17:40:01.431134 IP6 (hlim 255, next-header UDP (17) payload length: 110) fe80::5ad5:aff:feb3:6be1.5353 > ff02::fb.5353: [udp s                                                                                                                                                              um ok] 0 [1n] ANY (QM)? TRADFRI-Gateway-58d50ab36be1.local. ns: TRADFRI-Gateway-58d50ab36be1.local. [2m] A 10.1.0.18 (102)
17:40:01.431286 IP (tos 0x0, ttl 255, id 10, offset 0, flags [DF], proto UDP (17), length 130)
    10.1.0.18.5353 > 224.0.0.251.5353: [udp sum ok] 0 [1n] ANY (QM)? TRADFRI-Gateway-58d50ab36be1.local. ns: TRADFRI-Gateway-5                                                                                                                                                              8d50ab36be1.local. [2m] A 10.1.0.18 (102)
17:40:01.931124 IP6 (hlim 255, next-header UDP (17) payload length: 70) fe80::5ad5:aff:feb3:6be1.5353 > ff02::fb.5353: [udp su                                                                                                                                                              m ok] 0*- [0q] 1/0/0 TRADFRI-Gateway-58d50ab36be1.local. (Cache flush) [2m] A 10.1.0.18 (62)
17:40:01.931283 IP (tos 0x0, ttl 255, id 11, offset 0, flags [DF], proto UDP (17), length 90)
    10.1.0.18.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 1/0/0 TRADFRI-Gateway-58d50ab36be1.local. (Cache flush) [2m] A 10                                                                                                                                                              .1.0.18 (62)
17:40:02.931121 IP6 (hlim 255, next-header UDP (17) payload length: 70) fe80::5ad5:aff:feb3:6be1.5353 > ff02::fb.5353: [udp su                                                                                                                                                              m ok] 0*- [0q] 1/0/0 TRADFRI-Gateway-58d50ab36be1.local. (Cache flush) [2m] A 10.1.0.18 (62)
17:40:02.931274 IP (tos 0x0, ttl 255, id 12, offset 0, flags [DF], proto UDP (17), length 90)
    10.1.0.18.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 1/0/0 TRADFRI-Gateway-58d50ab36be1.local. (Cache flush) [2m] A 10                                                                                                                                                              .1.0.18 (62)
17:40:04.031146 IP6 (hlim 255, next-header UDP (17) payload length: 122) fe80::5ad5:aff:feb3:6be1.5353 > ff02::fb.5353: [udp s                                                                                                                                                              um ok] 0 [1n] ANY (QM)? TRADFRI-Gateway-58d50ab36be1.local. ns: TRADFRI-Gateway-58d50ab36be1.local. [2m] AAAA fe80::5ad5:aff:f                                                                                                                                                              eb3:6be1 (114)
17:40:04.031295 IP (tos 0x0, ttl 255, id 13, offset 0, flags [DF], proto UDP (17), length 142)
    10.1.0.18.5353 > 224.0.0.251.5353: [udp sum ok] 0 [1n] ANY (QM)? TRADFRI-Gateway-58d50ab36be1.local. ns: TRADFRI-Gateway-5                                                                                                                                                              8d50ab36be1.local. [2m] AAAA fe80::5ad5:aff:feb3:6be1 (114)
17:40:04.531128 IP6 (hlim 255, next-header UDP (17) payload length: 122) fe80::5ad5:aff:feb3:6be1.5353 > ff02::fb.5353: [udp s                                                                                                                                                              um ok] 0 [1n] ANY (QM)? TRADFRI-Gateway-58d50ab36be1.local. ns: TRADFRI-Gateway-58d50ab36be1.local. [2m] AAAA fe80::5ad5:aff:f                                                                                                                                                              eb3:6be1 (114)
17:40:04.531287 IP (tos 0x0, ttl 255, id 14, offset 0, flags [DF], proto UDP (17), length 142)
    10.1.0.18.5353 > 224.0.0.251.5353: [udp sum ok] 0 [1n] ANY (QM)? TRADFRI-Gateway-58d50ab36be1.local. ns: TRADFRI-Gateway-5                                                                                                                                                              8d50ab36be1.local. [2m] AAAA fe80::5ad5:aff:feb3:6be1 (114)
17:40:05.031129 IP6 (hlim 255, next-header UDP (17) payload length: 122) fe80::5ad5:aff:feb3:6be1.5353 > ff02::fb.5353: [udp s                                                                                                                                                              um ok] 0 [1n] ANY (QM)? TRADFRI-Gateway-58d50ab36be1.local. ns: TRADFRI-Gateway-58d50ab36be1.local. [2m] AAAA fe80::5ad5:aff:f                                                                                                                                                              eb3:6be1 (114)
17:40:05.031284 IP (tos 0x0, ttl 255, id 15, offset 0, flags [DF], proto UDP (17), length 142)
    10.1.0.18.5353 > 224.0.0.251.5353: [udp sum ok] 0 [1n] ANY (QM)? TRADFRI-Gateway-58d50ab36be1.local. ns: TRADFRI-Gateway-5                                                                                                                                                              8d50ab36be1.local. [2m] AAAA fe80::5ad5:aff:feb3:6be1 (114)
17:40:05.329108 IP6 (hlim 255, next-header ICMPv6 (58) payload length: 16) fe80::5ad5:aff:feb3:6be1 > ff02::2: [icmp6 sum ok]                                                                                                                                                               ICMP6, router solicitation, length 16
          source link-address option (1), length 8 (1): 58:d5:0a:b3:6b:e1
            0x0000:  58d5 0ab3 6be1
17:40:05.531117 IP6 (hlim 255, next-header UDP (17) payload length: 82) fe80::5ad5:aff:feb3:6be1.5353 > ff02::fb.5353: [udp su                                                                                                                                                              m ok] 0*- [0q] 1/0/0 TRADFRI-Gateway-58d50ab36be1.local. (Cache flush) [2m] AAAA fe80::5ad5:aff:feb3:6be1 (74)
17:40:05.531275 IP (tos 0x0, ttl 255, id 16, offset 0, flags [DF], proto UDP (17), length 102)
    10.1.0.18.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 1/0/0 TRADFRI-Gateway-58d50ab36be1.local. (Cache flush) [2m] AAAA                                                                                                                                                               fe80::5ad5:aff:feb3:6be1 (74)
17:40:05.650262 ARP, Ethernet (len 6), IPv4 (len 4), Request who-has 10.1.0.18 tell 10.1.0.1, length 28
17:40:05.650370 ARP, Ethernet (len 6), IPv4 (len 4), Reply 10.1.0.18 is-at 58:d5:0a:b3:6b:e1, length 46
17:40:06.531115 IP6 (hlim 255, next-header UDP (17) payload length: 82) fe80::5ad5:aff:feb3:6be1.5353 > ff02::fb.5353: [udp su                                                                                                                                                              m ok] 0*- [0q] 1/0/0 TRADFRI-Gateway-58d50ab36be1.local. (Cache flush) [2m] AAAA fe80::5ad5:aff:feb3:6be1 (74)
17:40:06.531273 IP (tos 0x0, ttl 255, id 17, offset 0, flags [DF], proto UDP (17), length 102)
    10.1.0.18.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 1/0/0 TRADFRI-Gateway-58d50ab36be1.local. (Cache flush) [2m] AAAA                                                                                                                                                               fe80::5ad5:aff:feb3:6be1 (74)
17:40:07.532006 IP (tos 0x0, ttl 255, id 18, offset 0, flags [DF], proto UDP (17), length 71)
    10.1.0.18.49749 > 10.1.0.1.53: [udp sum ok] 44596+ A? fw.ota.homesmart.ikea.net. (43)
17:40:07.532213 IP (tos 0x0, ttl 255, id 19, offset 0, flags [DF], proto UDP (17), length 71)
    10.1.0.18.49749 > 8.8.8.8.53: [udp sum ok] 29471+ A? fw.ota.homesmart.ikea.net. (43)
17:40:07.551572 IP (tos 0x0, ttl 64, id 55048, offset 0, flags [DF], proto UDP (17), length 175)
    10.1.0.1.53 > 10.1.0.18.49749: [udp sum ok] 44596 q: A? fw.ota.homesmart.ikea.net. 5/0/0 fw.ota.homesmart.ikea.net. [4m28s                                                                                                                                                              ] CNAME d262cmbxmzphsu.cloudfront.net., d262cmbxmzphsu.cloudfront.net. [59s] A 65.9.73.126, d262cmbxmzphsu.cloudfront.net. [59                                                                                                                                                              s] A 65.9.73.117, d262cmbxmzphsu.cloudfront.net. [59s] A 65.9.73.99, d262cmbxmzphsu.cloudfront.net. [59s] A 65.9.73.114 (147)
17:40:07.551750 IP (tos 0x0, ttl 128, id 20, offset 0, flags [none], proto TCP (6), length 48)
    10.1.0.18.49353 > 65.9.73.126.443: Flags [S], cksum 0xd201 (correct), seq 3979760328, win 7168, options [mss 1460,wscale 0                                                                                                                                                              ,eol], length 0
17:40:07.553184 IP (tos 0x80, ttl 124, id 40182, offset 0, flags [none], proto UDP (17), length 175)
    8.8.8.8.53 > 10.1.0.18.49749: [udp sum ok] 29471 q: A? fw.ota.homesmart.ikea.net. 5/0/0 fw.ota.homesmart.ikea.net. [4m26s]                                                                                                                                                               CNAME d262cmbxmzphsu.cloudfront.net., d262cmbxmzphsu.cloudfront.net. [59s] A 65.9.73.114, d262cmbxmzphsu.cloudfront.net. [59s                                                                                                                                                              ] A 65.9.73.117, d262cmbxmzphsu.cloudfront.net. [59s] A 65.9.73.126, d262cmbxmzphsu.cloudfront.net. [59s] A 65.9.73.99 (147)
17:40:07.553323 IP (tos 0x0, ttl 255, id 21, offset 0, flags [none], proto ICMP (1), length 56)
    10.1.0.18 > 8.8.8.8: ICMP 10.1.0.18 udp port 49749 unreachable, length 36
        IP (tos 0x80, ttl 124, id 40182, offset 0, flags [none], proto UDP (17), length 175)
    8.8.8.8.53 > 10.1.0.18.49749: [|domain]
17:40:07.557208 IP (tos 0x0, ttl 247, id 44087, offset 0, flags [none], proto TCP (6), length 48)
    65.9.73.126.443 > 10.1.0.18.49353: Flags [S.], cksum 0x5dc2 (correct), seq 3909920291, ack 3979760329, win 65535, options                                                                                                                                                               [mss 1450,nop,wscale 8], length 0
17:40:07.557340 IP (tos 0x0, ttl 128, id 22, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.49353 > 65.9.73.126.443: Flags [.], cksum 0x6d84 (correct), seq 1, ack 1, win 7168, length 0
17:40:07.557501 IP (tos 0x0, ttl 128, id 23, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.49353 > 65.9.73.126.443: Flags [F.], cksum 0x6d83 (correct), seq 1, ack 1, win 7168, length 0
17:40:07.562697 IP (tos 0x0, ttl 247, id 44088, offset 0, flags [none], proto TCP (6), length 40)
    65.9.73.126.443 > 10.1.0.18.49353: Flags [F.], cksum 0x8882 (correct), seq 1, ack 2, win 256, length 0
17:40:07.562824 IP (tos 0x0, ttl 128, id 24, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.49353 > 65.9.73.126.443: Flags [.], cksum 0x6d82 (correct), seq 2, ack 2, win 7168, length 0
17:40:09.329103 IP6 (hlim 255, next-header ICMPv6 (58) payload length: 16) fe80::5ad5:aff:feb3:6be1 > ff02::2: [icmp6 sum ok]                                                                                                                                                               ICMP6, router solicitation, length 16
          source link-address option (1), length 8 (1): 58:d5:0a:b3:6b:e1
            0x0000:  58d5 0ab3 6be1
17:40:23.294116 IP6 (hlim 255, next-header UDP (17) payload length: 142) fe80::5ad5:aff:feb3:6be1.5353 > ff02::fb.5353: [udp s                                                                                                                                                              um ok] 0 [1n] ANY (QM)? TRADFRI gateway._hap._tcp.local. ns: TRADFRI gateway._hap._tcp.local. [1h15m] SRV TRADFRI-Gateway-58d5                                                                                                                                                              0ab36be1.local.:80 0 0 (134)
17:40:23.294270 IP (tos 0x0, ttl 255, id 25, offset 0, flags [DF], proto UDP (17), length 162)
    10.1.0.18.5353 > 224.0.0.251.5353: [udp sum ok] 0 [1n] ANY (QM)? TRADFRI gateway._hap._tcp.local. ns: TRADFRI gateway._hap                                                                                                                                                              ._tcp.local. [1h15m] SRV TRADFRI-Gateway-58d50ab36be1.local.:80 0 0 (134)
17:40:23.794106 IP6 (hlim 255, next-header UDP (17) payload length: 142) fe80::5ad5:aff:feb3:6be1.5353 > ff02::fb.5353: [udp s                                                                                                                                                              um ok] 0 [1n] ANY (QM)? TRADFRI gateway._hap._tcp.local. ns: TRADFRI gateway._hap._tcp.local. [1h15m] SRV TRADFRI-Gateway-58d5                                                                                                                                                              0ab36be1.local.:80 0 0 (134)
17:40:23.794264 IP (tos 0x0, ttl 255, id 26, offset 0, flags [DF], proto UDP (17), length 162)
    10.1.0.18.5353 > 224.0.0.251.5353: [udp sum ok] 0 [1n] ANY (QM)? TRADFRI gateway._hap._tcp.local. ns: TRADFRI gateway._hap                                                                                                                                                              ._tcp.local. [1h15m] SRV TRADFRI-Gateway-58d50ab36be1.local.:80 0 0 (134)
17:40:24.294102 IP6 (hlim 255, next-header UDP (17) payload length: 142) fe80::5ad5:aff:feb3:6be1.5353 > ff02::fb.5353: [udp s                                                                                                                                                              um ok] 0 [1n] ANY (QM)? TRADFRI gateway._hap._tcp.local. ns: TRADFRI gateway._hap._tcp.local. [1h15m] SRV TRADFRI-Gateway-58d5                                                                                                                                                              0ab36be1.local.:80 0 0 (134)
17:40:24.294257 IP (tos 0x0, ttl 255, id 27, offset 0, flags [DF], proto UDP (17), length 162)
    10.1.0.18.5353 > 224.0.0.251.5353: [udp sum ok] 0 [1n] ANY (QM)? TRADFRI gateway._hap._tcp.local. ns: TRADFRI gateway._hap                                                                                                                                                              ._tcp.local. [1h15m] SRV TRADFRI-Gateway-58d50ab36be1.local.:80 0 0 (134)
17:40:24.794142 IP6 (hlim 255, next-header UDP (17) payload length: 404) fe80::5ad5:aff:feb3:6be1.5353 > ff02::fb.5353: [udp s                                                                                                                                                              um ok] 0*- [0q] 5/0/0 TRADFRI gateway._hap._tcp.local. (Cache flush) [1h15m] SRV TRADFRI-Gateway-58d50ab36be1.local.:80 0 0, T                                                                                                                                                              RADFRI-Gateway-58d50ab36be1.local. (Cache flush) [2m] A 10.1.0.18, TRADFRI-Gateway-58d50ab36be1.local. (Cache flush) [2m] AAAA                                                                                                                                                               fe80::5ad5:aff:feb3:6be1, _hap._tcp.local. [1h15m] PTR TRADFRI gateway._hap._tcp.local., TRADFRI gateway._hap._tcp.local. (Ca                                                                                                                                                              che flush) [1h15m] TXT "id=B3:51:FF:E1:EB:69" "md=TRADFRI gateway" "pv=1.1" "s#=1" "c#=1" "sf=1" "ff=1" "ci=2" "sh=AAAAAA==" (                                                                                                                                                              396)
17:40:24.794299 IP (tos 0x0, ttl 255, id 28, offset 0, flags [DF], proto UDP (17), length 424)
    10.1.0.18.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 5/0/0 TRADFRI gateway._hap._tcp.local. (Cache flush) [1h15m] SRV                                                                                                                                                               TRADFRI-Gateway-58d50ab36be1.local.:80 0 0, TRADFRI-Gateway-58d50ab36be1.local. (Cache flush) [2m] A 10.1.0.18, TRADFRI-Gatewa                                                                                                                                                              y-58d50ab36be1.local. (Cache flush) [2m] AAAA fe80::5ad5:aff:feb3:6be1, _hap._tcp.local. [1h15m] PTR TRADFRI gateway._hap._tcp                                                                                                                                                              .local., TRADFRI gateway._hap._tcp.local. (Cache flush) [1h15m] TXT "id=B3:51:FF:E1:EB:69" "md=TRADFRI gateway" "pv=1.1" "s#=1                                                                                                                                                              " "c#=1" "sf=1" "ff=1" "ci=2" "sh=AAAAAA==" (396)
17:40:25.794139 IP6 (hlim 255, next-header UDP (17) payload length: 404) fe80::5ad5:aff:feb3:6be1.5353 > ff02::fb.5353: [udp s                                                                                                                                                              um ok] 0*- [0q] 5/0/0 TRADFRI gateway._hap._tcp.local. (Cache flush) [1h15m] SRV TRADFRI-Gateway-58d50ab36be1.local.:80 0 0, T                                                                                                                                                              RADFRI-Gateway-58d50ab36be1.local. (Cache flush) [2m] A 10.1.0.18, TRADFRI-Gateway-58d50ab36be1.local. (Cache flush) [2m] AAAA                                                                                                                                                               fe80::5ad5:aff:feb3:6be1, _hap._tcp.local. [1h15m] PTR TRADFRI gateway._hap._tcp.local., TRADFRI gateway._hap._tcp.local. (Ca                                                                                                                                                              che flush) [1h15m] TXT "id=B3:51:FF:E1:EB:69" "md=TRADFRI gateway" "pv=1.1" "s#=1" "c#=1" "sf=1" "ff=1" "ci=2" "sh=AAAAAA==" (                                                                                                                                                              396)
17:40:25.794307 IP (tos 0x0, ttl 255, id 29, offset 0, flags [DF], proto UDP (17), length 424)
    10.1.0.18.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 5/0/0 TRADFRI gateway._hap._tcp.local. (Cache flush) [1h15m] SRV                                                                                                                                                               TRADFRI-Gateway-58d50ab36be1.local.:80 0 0, TRADFRI-Gateway-58d50ab36be1.local. (Cache flush) [2m] A 10.1.0.18, TRADFRI-Gatewa                                                                                                                                                              y-58d50ab36be1.local. (Cache flush) [2m] AAAA fe80::5ad5:aff:feb3:6be1, _hap._tcp.local. [1h15m] PTR TRADFRI gateway._hap._tcp                                                                                                                                                              .local., TRADFRI gateway._hap._tcp.local. (Cache flush) [1h15m] TXT "id=B3:51:FF:E1:EB:69" "md=TRADFRI gateway" "pv=1.1" "s#=1                                                                                                                                                              " "c#=1" "sf=1" "ff=1" "ci=2" "sh=AAAAAA==" (396)
17:40:26.794269 IP6 (hlim 255, next-header UDP (17) payload length: 404) fe80::5ad5:aff:feb3:6be1.5353 > ff02::fb.5353: [udp s                                                                                                                                                              um ok] 0*- [0q] 5/0/0 _hap._tcp.local. [1h15m] PTR TRADFRI gateway._hap._tcp.local., TRADFRI gateway._hap._tcp.local. [1h15m]                                                                                                                                                               TXT "id=B3:51:FF:E1:EB:69" "md=TRADFRI gateway" "pv=1.1" "s#=1" "c#=1" "sf=1" "ff=1" "ci=2" "sh=AAAAAA==", TRADFRI gateway._ha                                                                                                                                                              p._tcp.local. [2m] SRV TRADFRI-Gateway-58d50ab36be1.local.:80 0 0, TRADFRI-Gateway-58d50ab36be1.local. [2m] A 10.1.0.18, TRADF                                                                                                                                                              RI-Gateway-58d50ab36be1.local. [2m] AAAA fe80::5ad5:aff:feb3:6be1 (396)
17:40:26.794431 IP (tos 0x0, ttl 255, id 30, offset 0, flags [DF], proto UDP (17), length 424)
    10.1.0.18.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 5/0/0 _hap._tcp.local. [1h15m] PTR TRADFRI gateway._hap._tcp.loca                                                                                                                                                              l., TRADFRI gateway._hap._tcp.local. [1h15m] TXT "id=B3:51:FF:E1:EB:69" "md=TRADFRI gateway" "pv=1.1" "s#=1" "c#=1" "sf=1" "ff                                                                                                                                                              =1" "ci=2" "sh=AAAAAA==", TRADFRI gateway._hap._tcp.local. [2m] SRV TRADFRI-Gateway-58d50ab36be1.local.:80 0 0, TRADFRI-Gatewa                                                                                                                                                              y-58d50ab36be1.local. [2m] A 10.1.0.18, TRADFRI-Gateway-58d50ab36be1.local. [2m] AAAA fe80::5ad5:aff:feb3:6be1 (396)
17:40:26.815718 IP (tos 0x0, ttl 255, id 31, offset 0, flags [DF], proto UDP (17), length 71)
    10.1.0.18.50611 > 10.1.0.1.53: [udp sum ok] 58769+ A? fw.ota.homesmart.ikea.net. (43)
17:40:26.815926 IP (tos 0x0, ttl 255, id 32, offset 0, flags [DF], proto UDP (17), length 71)
    10.1.0.18.50611 > 8.8.8.8.53: [udp sum ok] 12659+ A? fw.ota.homesmart.ikea.net. (43)
17:40:26.816639 IP (tos 0x0, ttl 64, id 55822, offset 0, flags [DF], proto UDP (17), length 178)
    10.1.0.1.53 > 10.1.0.18.50611: [udp sum ok] 58769 q: A? fw.ota.homesmart.ikea.net. 5/0/0 fw.ota.homesmart.ikea.net. [4m9s]                                                                                                                                                               CNAME d262cmbxmzphsu.cloudfront.net., d262cmbxmzphsu.cloudfront.net. [40s] A 65.9.73.114, d262cmbxmzphsu.cloudfront.net. [40s                                                                                                                                                              ] A 65.9.73.99, d262cmbxmzphsu.cloudfront.net. [40s] A 65.9.73.117, d262cmbxmzphsu.cloudfront.net. [40s] A 65.9.73.126 (150)
17:40:26.816799 IP (tos 0x0, ttl 128, id 33, offset 0, flags [none], proto TCP (6), length 48)
    10.1.0.18.63220 > 65.9.73.114.80: Flags [S], cksum 0xb15b (correct), seq 1697367749, win 7168, options [mss 1460,wscale 0,                                                                                                                                                              eol], length 0
17:40:26.821945 IP (tos 0x0, ttl 247, id 30687, offset 0, flags [none], proto TCP (6), length 48)
    65.9.73.114.80 > 10.1.0.18.63220: Flags [S.], cksum 0x796f (correct), seq 3301477908, ack 1697367750, win 65535, options [                                                                                                                                                              mss 1450,nop,wscale 8], length 0
17:40:26.822065 IP (tos 0x0, ttl 128, id 34, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.63220 > 65.9.73.114.80: Flags [.], cksum 0x8931 (correct), seq 1, ack 1, win 7168, length 0
17:40:26.822188 IP (tos 0x0, ttl 128, id 35, offset 0, flags [none], proto TCP (6), length 220)
    10.1.0.18.63220 > 65.9.73.114.80: Flags [P.], cksum 0x64e9 (correct), seq 1:181, ack 1, win 7168, length 180: HTTP, length                                                                                                                                                              : 180
        GET /feed/version_info.json HTTP/1.0
        User-Agent: HertzClient/1.0 (GW (1).(8).(25); Id ae5ff982-b2a5-431a-a307-88d4d284744b)
        Host: fw.ota.homesmart.ikea.net
        Connection: close

17:40:26.822406 IP (tos 0x0, ttl 123, id 774, offset 0, flags [none], proto UDP (17), length 175)
    8.8.8.8.53 > 10.1.0.18.50611: [udp sum ok] 12659 q: A? fw.ota.homesmart.ikea.net. 5/0/0 fw.ota.homesmart.ikea.net. [4m9s]                                                                                                                                                               CNAME d262cmbxmzphsu.cloudfront.net., d262cmbxmzphsu.cloudfront.net. [40s] A 65.9.73.126, d262cmbxmzphsu.cloudfront.net. [40s]                                                                                                                                                               A 65.9.73.117, d262cmbxmzphsu.cloudfront.net. [40s] A 65.9.73.99, d262cmbxmzphsu.cloudfront.net. [40s] A 65.9.73.114 (147)
17:40:26.822518 IP (tos 0x0, ttl 255, id 36, offset 0, flags [none], proto ICMP (1), length 56)
    10.1.0.18 > 8.8.8.8: ICMP 10.1.0.18 udp port 50611 unreachable, length 36
        IP (tos 0x0, ttl 123, id 774, offset 0, flags [none], proto UDP (17), length 175)
    8.8.8.8.53 > 10.1.0.18.50611: [|domain]
17:40:26.827356 IP (tos 0x0, ttl 247, id 30688, offset 0, flags [none], proto TCP (6), length 40)
    65.9.73.114.80 > 10.1.0.18.63220: Flags [.], cksum 0xa378 (correct), seq 1, ack 181, win 261, length 0
17:40:26.914103 IP6 (hlim 255, next-header UDP (17) payload length: 144) fe80::5ad5:aff:feb3:6be1.5353 > ff02::fb.5353: [udp s                                                                                                                                                              um ok] 0 [1n] ANY (QM)? gw-58d50ab36be1._coap._udp.local. ns: gw-58d50ab36be1._coap._udp.local. [5m] SRV TRADFRI-Gateway-58d50                                                                                                                                                              ab36be1.local.:5684 0 0 (136)
17:40:26.914259 IP (tos 0x0, ttl 255, id 37, offset 0, flags [DF], proto UDP (17), length 164)
    10.1.0.18.5353 > 224.0.0.251.5353: [udp sum ok] 0 [1n] ANY (QM)? gw-58d50ab36be1._coap._udp.local. ns: gw-58d50ab36be1._co                                                                                                                                                              ap._udp.local. [5m] SRV TRADFRI-Gateway-58d50ab36be1.local.:5684 0 0 (136)
17:40:27.188710 IP (tos 0x0, ttl 247, id 30713, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.114.80 > 10.1.0.18.63220: Flags [.], cksum 0x0009 (correct), seq 1:1451, ack 181, win 261, length 1450: HTTP, leng                                                                                                                                                              th: 1450
        HTTP/1.1 200 OK
        Content-Type: application/json; charset=utf-8
        Content-Length: 6993
        Connection: close
        x-amz-id-2: UBYFnrEUuBQcqpfzR1XSkNUd2jLiG0MvYGkCRJhaJYlLmv3/qnz5KtoEuzVgxkEYvt7z3a+6jtg=
        x-amz-request-id: 2ACB257AECCAE6F4
        x-amz-replication-status: COMPLETED
        Last-Modified: Tue, 24 Nov 2020 11:58:35 GMT
        x-amz-version-id: CYG6dOrsYIzbxUFa_OCK.V.u4Wcs08xH
        Accept-Ranges: bytes
        Server: AmazonS3
        Date: Mon, 14 Dec 2020 01:00:59 GMT
        ETag: "4f9e909ba360e8b778bfc5ccae5e63f6"
        X-Cache: Hit from cloudfront
        Via: 1.1 cfe504a64f6a3eed0237f039e09f6185.cloudfront.net (CloudFront)
        X-Amz-Cf-Pop: AMS1-C1
        X-Amz-Cf-Id: xTGpmyr4ZJ5tJwPfrmIH780diTEN0cc31NQAVr2_RSd8bsJpNvxAow==

        [{"fw_binary_url":"http://fw.ota.homesmart.ikea.net/global/GW1.0/01.12.031/bin/10005777-6.1-TRADFRI-control-outlet-2.0                                                                                                                                                              .024.ota.ota.signed","fw_file_version_LSB":17955,"fw_file_version_MSB":8194,"fw_filesize":202110,"fw_image_type":4353,"fw_manu                                                                                                                                                              facturer_id":4476,"fw_type":2},{"fw_binary_url":"http://fw.ota.homesmart.ikea.net/global/GW1.0/01.12.031/bin/10035514-2.1-TRAD                                                                                                                                                              FRI-bulb-ws-2.3.050.ota.ota.signed","fw_file_version_LSB":1585,"fw_file_version_MSB":8965,"fw_filesize":207486,"fw_image_type"                                                                                                                                                              :8705,"fw_manufacturer_id":4476,"fw_type":2},{"fw_binary_url":"http://fw.ota.homesmart.ikea.net/global/GW1.0/01.12.031/bin/100                                                                                                                                                              05778-10.1-TRADFRI-onoff-shortcut-control-2.2.010.ota.ota.signed","fw_file_version_LSB":1585,"fw_file_version_MSB":8705,"fw_fi                                                                                                                                                              lesize":179838,"fw_i[!http]
17:40:27.188870 IP (tos 0x0, ttl 247, id 30714, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.114.80 > 10.1.0.18.63220: Flags [P.], cksum 0xffd9 (correct), seq 1451:2901, ack 181, win 261, length 1450: HTTP
17:40:27.188989 IP (tos 0x0, ttl 247, id 30715, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.114.80 > 10.1.0.18.63220: Flags [.], cksum 0x8510 (correct), seq 2901:4351, ack 181, win 261, length 1450: HTTP
17:40:27.189102 IP (tos 0x0, ttl 247, id 30716, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.114.80 > 10.1.0.18.63220: Flags [P.], cksum 0xb384 (correct), seq 4351:5801, ack 181, win 261, length 1450: HTTP
17:40:27.189147 IP (tos 0x0, ttl 128, id 38, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.63220 > 65.9.73.114.80: Flags [.], cksum 0x82d3 (correct), seq 181, ack 2901, win 5718, length 0
17:40:27.189437 IP (tos 0x0, ttl 128, id 39, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.63220 > 65.9.73.114.80: Flags [F.], cksum 0x82d2 (correct), seq 181, ack 4351, win 4268, length 0
17:40:27.194389 IP (tos 0x0, ttl 247, id 30717, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.114.80 > 10.1.0.18.63220: Flags [.], cksum 0xadb1 (correct), seq 5801:7251, ack 181, win 261, length 1450: HTTP
17:40:27.194572 IP (tos 0x0, ttl 247, id 30718, offset 0, flags [none], proto TCP (6), length 465)
    65.9.73.114.80 > 10.1.0.18.63220: Flags [FP.], cksum 0x61dc (correct), seq 7251:7676, ack 181, win 261, length 425: HTTP
17:40:27.194745 IP (tos 0x0, ttl 247, id 30719, offset 0, flags [none], proto TCP (6), length 40)
    65.9.73.114.80 > 10.1.0.18.63220: Flags [.], cksum 0x857b (correct), seq 7677, ack 182, win 261, length 0
17:40:27.194794 IP (tos 0x0, ttl 128, id 40, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.63220 > 65.9.73.114.80: Flags [.], cksum 0x82d1 (correct), seq 182, ack 7677, win 943, length 0
17:40:27.194962 IP (tos 0x0, ttl 255, id 41, offset 0, flags [DF], proto UDP (17), length 71)
    10.1.0.18.56855 > 10.1.0.1.53: [udp sum ok] 4288+ A? fw.ota.homesmart.ikea.net. (43)
17:40:27.195189 IP (tos 0x0, ttl 255, id 42, offset 0, flags [DF], proto UDP (17), length 71)
    10.1.0.18.56855 > 8.8.8.8.53: [udp sum ok] 61493+ A? fw.ota.homesmart.ikea.net. (43)
17:40:27.196149 IP (tos 0x0, ttl 64, id 55833, offset 0, flags [DF], proto UDP (17), length 178)
    10.1.0.1.53 > 10.1.0.18.56855: [udp sum ok] 4288 q: A? fw.ota.homesmart.ikea.net. 5/0/0 fw.ota.homesmart.ikea.net. [4m8s]                                                                                                                                                               CNAME d262cmbxmzphsu.cloudfront.net., d262cmbxmzphsu.cloudfront.net. [39s] A 65.9.73.126, d262cmbxmzphsu.cloudfront.net. [39s]                                                                                                                                                               A 65.9.73.114, d262cmbxmzphsu.cloudfront.net. [39s] A 65.9.73.99, d262cmbxmzphsu.cloudfront.net. [39s] A 65.9.73.117 (150)
17:40:27.204500 IP (tos 0x0, ttl 247, id 49008, offset 0, flags [none], proto TCP (6), length 48)
    65.9.73.126.80 > 10.1.0.18.52439: Flags [S.], cksum 0x7af0 (correct), seq 551020398, ack 2219580109, win 65535, options [m                                                                                                                                                              ss 1450,nop,wscale 8], length 0
17:40:27.204737 IP (tos 0x0, ttl 128, id 44, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.52439 > 65.9.73.126.80: Flags [.], cksum 0x8ab2 (correct), seq 1, ack 1, win 7168, length 0
17:40:27.204889 IP (tos 0x0, ttl 128, id 45, offset 0, flags [none], proto TCP (6), length 220)
    10.1.0.18.52439 > 65.9.73.126.80: Flags [P.], cksum 0x666a (correct), seq 1:181, ack 1, win 7168, length 180: HTTP, length                                                                                                                                                              : 180
        GET /feed/version_info.json HTTP/1.0
        User-Agent: HertzClient/1.0 (GW (1).(8).(25); Id ae5ff982-b2a5-431a-a307-88d4d284744b)
        Host: fw.ota.homesmart.ikea.net
        Connection: close

17:40:27.210628 IP (tos 0x80, ttl 124, id 58210, offset 0, flags [none], proto UDP (17), length 175)
    8.8.8.8.53 > 10.1.0.18.56855: [udp sum ok] 61493 q: A? fw.ota.homesmart.ikea.net. 5/0/0 fw.ota.homesmart.ikea.net. [3m14s]                                                                                                                                                               CNAME d262cmbxmzphsu.cloudfront.net., d262cmbxmzphsu.cloudfront.net. [59s] A 65.9.73.99, d262cmbxmzphsu.cloudfront.net. [59s]                                                                                                                                                               A 65.9.73.126, d262cmbxmzphsu.cloudfront.net. [59s] A 65.9.73.114, d262cmbxmzphsu.cloudfront.net. [59s] A 65.9.73.117 (147)
17:40:27.210860 IP (tos 0x0, ttl 255, id 46, offset 0, flags [none], proto ICMP (1), length 56)
    10.1.0.18 > 8.8.8.8: ICMP 10.1.0.18 udp port 56855 unreachable, length 36
        IP (tos 0x80, ttl 124, id 58210, offset 0, flags [none], proto UDP (17), length 175)
    8.8.8.8.53 > 10.1.0.18.56855: [|domain]
17:40:27.213018 IP (tos 0x0, ttl 247, id 49009, offset 0, flags [none], proto TCP (6), length 40)
    65.9.73.126.80 > 10.1.0.18.52439: Flags [.], cksum 0xa4f9 (correct), seq 1, ack 181, win 261, length 0
17:40:27.414105 IP6 (hlim 255, next-header UDP (17) payload length: 144) fe80::5ad5:aff:feb3:6be1.5353 > ff02::fb.5353: [udp s                                                                                                                                                              um ok] 0 [1n] ANY (QM)? gw-58d50ab36be1._coap._udp.local. ns: gw-58d50ab36be1._coap._udp.local. [5m] SRV TRADFRI-Gateway-58d50                                                                                                                                                              ab36be1.local.:5684 0 0 (136)
17:40:27.414265 IP (tos 0x0, ttl 255, id 47, offset 0, flags [DF], proto UDP (17), length 164)
    10.1.0.18.5353 > 224.0.0.251.5353: [udp sum ok] 0 [1n] ANY (QM)? gw-58d50ab36be1._coap._udp.local. ns: gw-58d50ab36be1._co                                                                                                                                                              ap._udp.local. [5m] SRV TRADFRI-Gateway-58d50ab36be1.local.:5684 0 0 (136)
17:40:27.572595 IP (tos 0x0, ttl 247, id 49046, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.126.80 > 10.1.0.18.52439: Flags [.], cksum 0x1026 (correct), seq 1:1451, ack 181, win 261, length 1450: HTTP, leng                                                                                                                                                              th: 1450
        HTTP/1.1 200 OK
        Content-Type: application/json; charset=utf-8
        Content-Length: 6993
        Connection: close
        x-amz-id-2: xE0BOZ7vRkCToxtuWnSrCFDwPHx8ssYsEv2+krlAjMurBmHvVaqUgOr7e1aP+Smzf3htAyBQvIM=
        x-amz-request-id: DC136DE29B9112F1
        x-amz-replication-status: COMPLETED
        Last-Modified: Tue, 24 Nov 2020 11:58:35 GMT
        x-amz-version-id: CYG6dOrsYIzbxUFa_OCK.V.u4Wcs08xH
        Accept-Ranges: bytes
        Server: AmazonS3
        Date: Mon, 14 Dec 2020 17:00:34 GMT
        ETag: "4f9e909ba360e8b778bfc5ccae5e63f6"
        X-Cache: Hit from cloudfront
        Via: 1.1 e10153740ff95eb4d0c9f3172baeb43e.cloudfront.net (CloudFront)
        X-Amz-Cf-Pop: AMS1-C1
        X-Amz-Cf-Id: WQYTpP7NalOuMFZkC0DG6vFPWpseamQhrX_1i4bHqalh6JPii6quPw==

        [{"fw_binary_url":"http://fw.ota.homesmart.ikea.net/global/GW1.0/01.12.031/bin/10005777-6.1-TRADFRI-control-outlet-2.0                                                                                                                                                              .024.ota.ota.signed","fw_file_version_LSB":17955,"fw_file_version_MSB":8194,"fw_filesize":202110,"fw_image_type":4353,"fw_manu                                                                                                                                                              facturer_id":4476,"fw_type":2},{"fw_binary_url":"http://fw.ota.homesmart.ikea.net/global/GW1.0/01.12.031/bin/10035514-2.1-TRAD                                                                                                                                                              FRI-bulb-ws-2.3.050.ota.ota.signed","fw_file_version_LSB":1585,"fw_file_version_MSB":8965,"fw_filesize":207486,"fw_image_type"                                                                                                                                                              :8705,"fw_manufacturer_id":4476,"fw_type":2},{"fw_binary_url":"http://fw.ota.homesmart.ikea.net/global/GW1.0/01.12.031/bin/100                                                                                                                                                              05778-10.1-TRADFRI-onoff-shortcut-control-2.2.010.ota.ota.signed","fw_file_version_LSB":1585,"fw_file_version_MSB":8705,"fw_fi                                                                                                                                                              lesize":179838,"fw_i[!http]
17:40:27.572769 IP (tos 0x0, ttl 247, id 49047, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.126.80 > 10.1.0.18.52439: Flags [P.], cksum 0x015b (correct), seq 1451:2901, ack 181, win 261, length 1450: HTTP
17:40:27.572892 IP (tos 0x0, ttl 247, id 49048, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.126.80 > 10.1.0.18.52439: Flags [.], cksum 0x8691 (correct), seq 2901:4351, ack 181, win 261, length 1450: HTTP
17:40:27.573008 IP (tos 0x0, ttl 247, id 49049, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.126.80 > 10.1.0.18.52439: Flags [P.], cksum 0xb505 (correct), seq 4351:5801, ack 181, win 261, length 1450: HTTP
17:40:27.573050 IP (tos 0x0, ttl 128, id 48, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.52439 > 65.9.73.126.80: Flags [.], cksum 0x8454 (correct), seq 181, ack 2901, win 5718, length 0
17:40:27.573263 IP (tos 0x0, ttl 128, id 49, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.52439 > 65.9.73.126.80: Flags [.], cksum 0x7356 (correct), seq 181, ack 5801, win 7168, length 0
17:40:27.573418 IP (tos 0x0, ttl 128, id 50, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.52439 > 65.9.73.126.80: Flags [.], cksum 0x7356 (correct), seq 181, ack 5801, win 7168, length 0
17:40:27.581211 IP (tos 0x0, ttl 247, id 49050, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.126.80 > 10.1.0.18.52439: Flags [.], cksum 0xaf32 (correct), seq 5801:7251, ack 181, win 261, length 1450: HTTP
17:40:27.581432 IP (tos 0x0, ttl 247, id 49051, offset 0, flags [none], proto TCP (6), length 465)
    65.9.73.126.80 > 10.1.0.18.52439: Flags [FP.], cksum 0x635d (correct), seq 7251:7676, ack 181, win 261, length 425: HTTP
17:40:27.581687 IP (tos 0x0, ttl 128, id 51, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.52439 > 65.9.73.126.80: Flags [.], cksum 0x6c02 (correct), seq 181, ack 7677, win 7168, length 0
17:40:27.581855 IP (tos 0x0, ttl 128, id 52, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.52439 > 65.9.73.126.80: Flags [F.], cksum 0x6c01 (correct), seq 181, ack 7677, win 7168, length 0
17:40:27.590072 IP (tos 0x0, ttl 247, id 0, offset 0, flags [DF], proto TCP (6), length 40)
    65.9.73.126.80 > 10.1.0.18.52439: Flags [.], cksum 0x86fc (correct), seq 7677, ack 182, win 261, length 0
17:40:27.819298 IP (tos 0x0, ttl 255, id 53, offset 0, flags [DF], proto UDP (17), length 71)
    10.1.0.18.59981 > 10.1.0.1.53: [udp sum ok] 31036+ A? fw.ota.homesmart.ikea.net. (43)
17:40:27.819504 IP (tos 0x0, ttl 255, id 54, offset 0, flags [DF], proto UDP (17), length 71)
    10.1.0.18.59981 > 8.8.8.8.53: [udp sum ok] 39430+ A? fw.ota.homesmart.ikea.net. (43)
17:40:27.819957 IP (tos 0x0, ttl 64, id 55851, offset 0, flags [DF], proto UDP (17), length 178)
    10.1.0.1.53 > 10.1.0.18.59981: [udp sum ok] 31036 q: A? fw.ota.homesmart.ikea.net. 5/0/0 fw.ota.homesmart.ikea.net. [4m8s]                                                                                                                                                               CNAME d262cmbxmzphsu.cloudfront.net., d262cmbxmzphsu.cloudfront.net. [39s] A 65.9.73.117, d262cmbxmzphsu.cloudfront.net. [39s                                                                                                                                                              ] A 65.9.73.126, d262cmbxmzphsu.cloudfront.net. [39s] A 65.9.73.114, d262cmbxmzphsu.cloudfront.net. [39s] A 65.9.73.99 (150)
17:40:27.820126 IP (tos 0x0, ttl 128, id 55, offset 0, flags [none], proto TCP (6), length 48)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [S], cksum 0xeba2 (correct), seq 4163966902, win 7168, options [mss 1460,wscale 0,                                                                                                                                                              eol], length 0
17:40:27.825610 IP (tos 0x0, ttl 247, id 29009, offset 0, flags [none], proto TCP (6), length 48)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [S.], cksum 0x3f6f (correct), seq 1235385730, ack 4163966903, win 65535, options [                                                                                                                                                              mss 1450,nop,wscale 8], length 0
17:40:27.825845 IP (tos 0x0, ttl 128, id 56, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x4f31 (correct), seq 1, ack 1, win 7168, length 0
17:40:27.825999 IP (tos 0x0, ttl 128, id 57, offset 0, flags [none], proto TCP (6), length 309)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [P.], cksum 0xec7c (correct), seq 1:270, ack 1, win 7168, length 269: HTTP, length                                                                                                                                                              : 269
        GET /global/GW1.0/01.12.031/bin/10032198-2.2-TRADFRI-gateway-1.12.31.p.elf.sig.ota.signed HTTP/1.0
        User-Agent: HertzClient/1.0 (GW (1).(8).(25); Id ae5ff982-b2a5-431a-a307-88d4d284744b)
        Host: fw.ota.homesmart.ikea.net
        Range: bytes=0-16383
        Connection: keep-alive

17:40:27.829014 IP (tos 0x0, ttl 123, id 40583, offset 0, flags [none], proto UDP (17), length 175)
    8.8.8.8.53 > 10.1.0.18.59981: [udp sum ok] 39430 q: A? fw.ota.homesmart.ikea.net. 5/0/0 fw.ota.homesmart.ikea.net. [4m6s]                                                                                                                                                               CNAME d262cmbxmzphsu.cloudfront.net., d262cmbxmzphsu.cloudfront.net. [39s] A 65.9.73.114, d262cmbxmzphsu.cloudfront.net. [39s]                                                                                                                                                               A 65.9.73.117, d262cmbxmzphsu.cloudfront.net. [39s] A 65.9.73.126, d262cmbxmzphsu.cloudfront.net. [39s] A 65.9.73.99 (147)
17:40:27.829142 IP (tos 0x0, ttl 255, id 58, offset 0, flags [none], proto ICMP (1), length 56)
    10.1.0.18 > 8.8.8.8: ICMP 10.1.0.18 udp port 59981 unreachable, length 36
        IP (tos 0x0, ttl 123, id 40583, offset 0, flags [none], proto UDP (17), length 175)
    8.8.8.8.53 > 10.1.0.18.59981: [|domain]
17:40:27.831303 IP (tos 0x0, ttl 247, id 29010, offset 0, flags [none], proto TCP (6), length 40)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x691f (correct), seq 1, ack 270, win 261, length 0
17:40:27.914195 IP6 (hlim 255, next-header UDP (17) payload length: 144) fe80::5ad5:aff:feb3:6be1.5353 > ff02::fb.5353: [udp s                                                                                                                                                              um ok] 0 [1n] ANY (QM)? gw-58d50ab36be1._coap._udp.local. ns: gw-58d50ab36be1._coap._udp.local. [5m] SRV TRADFRI-Gateway-58d50                                                                                                                                                              ab36be1.local.:5684 0 0 (136)
17:40:27.914358 IP (tos 0x0, ttl 255, id 59, offset 0, flags [DF], proto UDP (17), length 164)
    10.1.0.18.5353 > 224.0.0.251.5353: [udp sum ok] 0 [1n] ANY (QM)? gw-58d50ab36be1._coap._udp.local. ns: gw-58d50ab36be1._co                                                                                                                                                              ap._udp.local. [5m] SRV TRADFRI-Gateway-58d50ab36be1.local.:5684 0 0 (136)
17:40:28.238032 IP (tos 0x0, ttl 247, id 29039, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x12f4 (correct), seq 1:1451, ack 270, win 261, length 1450: HTTP, leng                                                                                                                                                              th: 1450
        HTTP/1.1 206 Partial Content
        Content-Type: application/octet-stream
        Content-Length: 16384
        Connection: keep-alive
        x-amz-id-2: z8UHmX5DhLSMUklEbnGKSrTxUrCup9adtoQAGBh6vWBZOdIm/PBjzD1XY7nGlm+IMPL4P96pbcs=
        x-amz-request-id: D32529443F17BFEE
        x-amz-replication-status: COMPLETED
        Last-Modified: Tue, 24 Nov 2020 11:58:35 GMT
        x-amz-version-id: Q7SCltPeHFFpYmqCkNIdy.Hws_ZUJEhk
        Accept-Ranges: bytes
        Server: AmazonS3
        Date: Mon, 14 Dec 2020 14:40:00 GMT
        ETag: "6504c28dfcdebd0a5dd533ef250f1dfc"
        Content-Range: bytes 0-16383/829224
        X-Cache: Hit from cloudfront
        Via: 1.1 d143bdfb7cce4cf7ec0bcf9ec13e5915.cloudfront.net (CloudFront)
        X-Amz-Cf-Pop: AMS1-C1
        X-Amz-Cf-Id: hCyeLrXFtnVdlQgQm1co23o1Lj0teXteczF2BIx3qjBWmGViOvkTfw==

17:40:28.238192 IP (tos 0x0, ttl 247, id 29040, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0x1989 (correct), seq 1451:2901, ack 270, win 261, length 1450: HTTP
17:40:28.238310 IP (tos 0x0, ttl 247, id 29041, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0xdf27 (correct), seq 2901:4351, ack 270, win 261, length 1450: HTTP
17:40:28.238422 IP (tos 0x0, ttl 247, id 29042, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0xfa9d (correct), seq 4351:5801, ack 270, win 261, length 1450: HTTP
17:40:28.238464 IP (tos 0x0, ttl 128, id 60, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x487a (correct), seq 270, ack 2901, win 5718, length 0
17:40:28.238684 IP (tos 0x0, ttl 128, id 61, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x377c (correct), seq 270, ack 5801, win 7168, length 0
17:40:28.238840 IP (tos 0x0, ttl 128, id 62, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x377c (correct), seq 270, ack 5801, win 7168, length 0
17:40:28.243680 IP (tos 0x0, ttl 247, id 29043, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x6ac8 (correct), seq 5801:7251, ack 270, win 261, length 1450: HTTP
17:40:28.243809 IP (tos 0x0, ttl 247, id 29044, offset 0, flags [none], proto TCP (6), length 1408)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0xde68 (correct), seq 7251:8619, ack 270, win 261, length 1368: HTTP
17:40:28.249505 IP (tos 0x0, ttl 247, id 29048, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x0c31 (correct), seq 11601:13051, ack 270, win 261, length 1450: HTTP
17:40:28.249673 IP (tos 0x0, ttl 247, id 29049, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0xdff0 (correct), seq 13051:14501, ack 270, win 261, length 1450: HTTP
17:40:28.249895 IP (tos 0x0, ttl 128, id 65, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x1b2a (correct), seq 270, ack 13051, win 7168, length 0
17:40:28.250127 IP (tos 0x0, ttl 247, id 29050, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0xed0a (correct), seq 14501:15951, ack 270, win 261, length 1450: HTTP
17:40:28.250325 IP (tos 0x0, ttl 247, id 29051, offset 0, flags [none], proto TCP (6), length 1205)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0xd657 (correct), seq 15951:17116, ack 270, win 261, length 1165: HTTP
17:40:28.250382 IP (tos 0x0, ttl 128, id 66, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x0fd6 (correct), seq 270, ack 15951, win 7168, length 0
17:40:28.251143 IP (tos 0x0, ttl 128, id 67, offset 0, flags [none], proto TCP (6), length 315)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [P.], cksum 0x07e8 (correct), seq 270:545, ack 17116, win 7168, length 275: HTTP,                                                                                                                                                               length: 275
        GET /global/GW1.0/01.12.031/bin/10032198-2.2-TRADFRI-gateway-1.12.31.p.elf.sig.ota.signed HTTP/1.0
        User-Agent: HertzClient/1.0 (GW (1).(8).(25); Id ae5ff982-b2a5-431a-a307-88d4d284744b)
        Host: fw.ota.homesmart.ikea.net
        Range: bytes=828712-845095
        Connection: keep-alive

17:40:28.256400 IP (tos 0x0, ttl 247, id 29052, offset 0, flags [none], proto TCP (6), length 40)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x252d (correct), seq 17116, ack 545, win 265, length 0
17:40:28.414136 IP6 (hlim 255, next-header UDP (17) payload length: 339) fe80::5ad5:aff:feb3:6be1.5353 > ff02::fb.5353: [udp s                                                                                                                                                              um ok] 0*- [0q] 5/0/0 gw-58d50ab36be1._coap._udp.local. (Cache flush) [5m] SRV TRADFRI-Gateway-58d50ab36be1.local.:5684 0 0, T                                                                                                                                                              RADFRI-Gateway-58d50ab36be1.local. (Cache flush) [2m] A 10.1.0.18, TRADFRI-Gateway-58d50ab36be1.local. (Cache flush) [2m] AAAA                                                                                                                                                               fe80::5ad5:aff:feb3:6be1, _coap._udp.local. [5m] PTR gw-58d50ab36be1._coap._udp.local., gw-58d50ab36be1._coap._udp.local. (Ca                                                                                                                                                              che flush) [5m] TXT "version=1.8.25" (331)
17:40:28.414305 IP (tos 0x0, ttl 255, id 68, offset 0, flags [DF], proto UDP (17), length 359)
    10.1.0.18.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 5/0/0 gw-58d50ab36be1._coap._udp.local. (Cache flush) [5m] SRV TR                                                                                                                                                              ADFRI-Gateway-58d50ab36be1.local.:5684 0 0, TRADFRI-Gateway-58d50ab36be1.local. (Cache flush) [2m] A 10.1.0.18, TRADFRI-Gatewa                                                                                                                                                              y-58d50ab36be1.local. (Cache flush) [2m] AAAA fe80::5ad5:aff:feb3:6be1, _coap._udp.local. [5m] PTR gw-58d50ab36be1._coap._udp.                                                                                                                                                              local., gw-58d50ab36be1._coap._udp.local. (Cache flush) [5m] TXT "version=1.8.25" (331)
17:40:28.621062 IP (tos 0x0, ttl 247, id 29061, offset 0, flags [none], proto TCP (6), length 775)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0x8f30 (correct), seq 17116:17851, ack 545, win 265, length 735: HTTP,                                                                                                                                                               length: 735
        HTTP/1.1 206 Partial Content
        Content-Type: application/octet-stream
        Content-Length: 512
        Connection: keep-alive
        x-amz-id-2: z8UHmX5DhLSMUklEbnGKSrTxUrCup9adtoQAGBh6vWBZOdIm/PBjzD1XY7nGlm+IMPL4P96pbcs=
        x-amz-request-id: D32529443F17BFEE
        x-amz-replication-status: COMPLETED
        Last-Modified: Tue, 24 Nov 2020 11:58:35 GMT
        x-amz-version-id: Q7SCltPeHFFpYmqCkNIdy.Hws_ZUJEhk
        Accept-Ranges: bytes
        Server: AmazonS3
        Date: Mon, 14 Dec 2020 14:40:00 GMT
        ETag: "6504c28dfcdebd0a5dd533ef250f1dfc"
        Content-Range: bytes 828712-829223/829224
        X-Cache: Hit from cloudfront
        Via: 1.1 d143bdfb7cce4cf7ec0bcf9ec13e5915.cloudfront.net (CloudFront)
        X-Amz-Cf-Pop: AMS1-C1
        X-Amz-Cf-Id: Xy2mbrAfrPdi6uvoC9uaBQLMnv5GOZBYTI1sZMBvL1TTCy__fZ1X4w==

17:40:28.621261 IP (tos 0x0, ttl 128, id 69, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x0757 (correct), seq 545, ack 17851, win 7168, length 0
17:40:28.621581 IP (tos 0x0, ttl 247, id 29062, offset 0, flags [none], proto TCP (6), length 552)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0x27f2 (correct), seq 17851:18363, ack 545, win 265, length 512: HTTP
17:40:28.655300 IP (tos 0x0, ttl 128, id 70, offset 0, flags [none], proto TCP (6), length 312)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [P.], cksum 0x871c (correct), seq 545:817, ack 18363, win 7168, length 272: HTTP,                                                                                                                                                               length: 272
        GET /global/GW1.0/01.12.031/bin/10032198-2.2-TRADFRI-gateway-1.12.31.p.elf.sig.ota.signed HTTP/1.0
        User-Agent: HertzClient/1.0 (GW (1).(8).(25); Id ae5ff982-b2a5-431a-a307-88d4d284744b)
        Host: fw.ota.homesmart.ikea.net
        Range: bytes=1672-18055
        Connection: keep-alive

17:40:28.660588 IP (tos 0x0, ttl 247, id 29065, offset 0, flags [none], proto TCP (6), length 40)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x1f3a (correct), seq 18363, ack 817, win 269, length 0
17:40:29.036062 IP (tos 0x0, ttl 247, id 29088, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x37b2 (correct), seq 18363:19813, ack 817, win 269, length 1450: HTTP,                                                                                                                                                               length: 1450
        HTTP/1.1 206 Partial Content
        Content-Type: application/octet-stream
        Content-Length: 16384
        Connection: keep-alive
        x-amz-id-2: z8UHmX5DhLSMUklEbnGKSrTxUrCup9adtoQAGBh6vWBZOdIm/PBjzD1XY7nGlm+IMPL4P96pbcs=
        x-amz-request-id: D32529443F17BFEE
        x-amz-replication-status: COMPLETED
        Last-Modified: Tue, 24 Nov 2020 11:58:35 GMT
        x-amz-version-id: Q7SCltPeHFFpYmqCkNIdy.Hws_ZUJEhk
        Accept-Ranges: bytes
        Server: AmazonS3
        Date: Mon, 14 Dec 2020 14:40:00 GMT
        ETag: "6504c28dfcdebd0a5dd533ef250f1dfc"
        Content-Range: bytes 1672-18055/829224
        X-Cache: Hit from cloudfront
        Via: 1.1 d143bdfb7cce4cf7ec0bcf9ec13e5915.cloudfront.net (CloudFront)
        X-Amz-Cf-Pop: AMS1-C1
        X-Amz-Cf-Id: j3y0VP9vnQ0OtJPDW5tZ-0wjUI6BmNTYMXrmGNJ2hvwSIIx4CmdT6g==

17:40:29.036240 IP (tos 0x0, ttl 247, id 29089, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0xab46 (correct), seq 19813:21263, ack 817, win 269, length 1450: HTTP
17:40:29.036448 IP (tos 0x0, ttl 247, id 29090, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x8c38 (correct), seq 21263:22713, ack 817, win 269, length 1450: HTTP
17:40:29.036629 IP (tos 0x0, ttl 247, id 29091, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0xfeb4 (correct), seq 22713:24163, ack 817, win 269, length 1450: HTTP
17:40:29.036678 IP (tos 0x0, ttl 128, id 71, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0xfe9c (correct), seq 817, ack 19813, win 7168, length 0
17:40:29.036856 IP (tos 0x0, ttl 128, id 72, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0xf348 (correct), seq 817, ack 22713, win 7168, length 0
17:40:29.042001 IP (tos 0x0, ttl 247, id 29092, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0xce3b (correct), seq 24163:25613, ack 817, win 269, length 1450: HTTP
17:40:29.042180 IP (tos 0x0, ttl 247, id 29093, offset 0, flags [none], proto TCP (6), length 1408)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0x1f88 (correct), seq 25613:26981, ack 817, win 269, length 1368: HTTP
17:40:29.042389 IP (tos 0x0, ttl 247, id 29094, offset 0, flags [none], proto TCP (6), length 122)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0xe25d (correct), seq 26981:27063, ack 817, win 269, length 82: HTTP
17:40:29.042565 IP (tos 0x0, ttl 247, id 29095, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x7913 (correct), seq 27063:28513, ack 817, win 269, length 1450: HTTP
17:40:29.042614 IP (tos 0x0, ttl 128, id 73, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0xe7f4 (correct), seq 817, ack 25613, win 7168, length 0
17:40:29.042909 IP (tos 0x0, ttl 247, id 29096, offset 0, flags [none], proto TCP (6), length 1408)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0x3621 (correct), seq 28513:29881, ack 817, win 269, length 1368: HTTP
17:40:29.042957 IP (tos 0x0, ttl 128, id 74, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0xe24a (correct), seq 817, ack 27063, win 7168, length 0
17:40:29.043414 IP (tos 0x0, ttl 128, id 75, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0xd748 (correct), seq 817, ack 29881, win 7168, length 0
17:40:29.047868 IP (tos 0x0, ttl 247, id 29098, offset 0, flags [none], proto TCP (6), length 122)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0x84d9 (correct), seq 29881:29963, ack 817, win 269, length 82: HTTP
17:40:29.048424 IP (tos 0x0, ttl 247, id 29099, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x806c (correct), seq 29963:31413, ack 817, win 269, length 1450: HTTP
17:40:29.048612 IP (tos 0x0, ttl 247, id 29100, offset 0, flags [none], proto TCP (6), length 1408)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0x1670 (correct), seq 31413:32781, ack 817, win 269, length 1368: HTTP
17:40:29.048797 IP (tos 0x0, ttl 247, id 29101, offset 0, flags [none], proto TCP (6), length 122)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x21ac (correct), seq 32781:32863, ack 817, win 269, length 82: HTTP
17:40:29.048839 IP (tos 0x0, ttl 128, id 76, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0xd14c (correct), seq 817, ack 31413, win 7168, length 0
17:40:29.049013 IP (tos 0x0, ttl 128, id 77, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0xcba2 (correct), seq 817, ack 32863, win 7168, length 0
17:40:29.049322 IP (tos 0x0, ttl 247, id 29102, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x155e (correct), seq 32863:34313, ack 817, win 269, length 1450: HTTP
17:40:29.049505 IP (tos 0x0, ttl 247, id 29103, offset 0, flags [none], proto TCP (6), length 1208)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0x6ac5 (correct), seq 34313:35481, ack 817, win 269, length 1168: HTTP
17:40:29.049782 IP (tos 0x0, ttl 128, id 78, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0xc168 (correct), seq 817, ack 35481, win 7168, length 0
17:40:29.051457 IP (tos 0x0, ttl 255, id 56319, offset 0, flags [DF], proto UDP (17), length 68)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0 PTR (QM)? _googlezone._tcp.local. (40)
17:40:29.053657 IP (tos 0x0, ttl 255, id 56320, offset 0, flags [DF], proto UDP (17), length 105)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0 SRV (QM)? 3777e026-f001-51e2-50f0-cf3c65a3883d._googlezone._tcp.local. (7                                                                                                                                                              7)
17:40:29.057193 IP (tos 0x0, ttl 255, id 56321, offset 0, flags [DF], proto UDP (17), length 301)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 4/0/0 _googlezone._tcp.local. [2m] PTR 3777e026-f001-51e2-50f0-cf3                                                                                                                                                              c65a3883d._googlezone._tcp.local., 3777e026-f001-51e2-50f0-cf3c65a3883d.local. (Cache flush) [2m] A 172.17.114.27, 3777e026-f0                                                                                                                                                              01-51e2-50f0-cf3c65a3883d._googlezone._tcp.local. (Cache flush) [2m] SRV 3777e026-f001-51e2-50f0-cf3c65a3883d.local.:10001 610                                                                                                                                                               6, 3777e026-f001-51e2-50f0-cf3c65a3883d._googlezone._tcp.local. (Cache flush) [1h15m] TXT "id=DFE00222F401A69E6326485C9B3A708                                                                                                                                                              2" "e63b80d7-28e4-4ebf-9ba3-0ce60e73e8ff=0|Beneden" "__common_time__=0|0" (273)
17:40:29.123313 IP (tos 0x0, ttl 255, id 56323, offset 0, flags [DF], proto UDP (17), length 105)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0 SRV (QM)? e8b58877-627a-8cea-281b-68f6f4a17d69._googlezone._tcp.local. (7                                                                                                                                                              7)
17:40:29.131844 IP (tos 0x0, ttl 255, id 56324, offset 0, flags [DF], proto UDP (17), length 303)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 4/0/0 _googlezone._tcp.local. [2m] PTR e8b58877-627a-8cea-281b-68f                                                                                                                                                              6f4a17d69._googlezone._tcp.local., e8b58877-627a-8cea-281b-68f6f4a17d69.local. (Cache flush) [2m] A 172.17.114.31, e8b58877-62                                                                                                                                                              7a-8cea-281b-68f6f4a17d69._googlezone._tcp.local. (Cache flush) [2m] SRV e8b58877-627a-8cea-281b-68f6f4a17d69.local.:10001 610                                                                                                                                                               6, e8b58877-627a-8cea-281b-68f6f4a17d69._googlezone._tcp.local. (Cache flush) [1h15m] TXT "id=C4D26B8C90E081C1D8DB77EB7294BDA                                                                                                                                                              9" "93d01926-c9e0-4458-b6bc-515a347c3ecc=0|Binnen" "__common_time__=1|7380" (275)
17:40:29.167632 IP (tos 0x0, ttl 255, id 56326, offset 0, flags [DF], proto UDP (17), length 401)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 4/0/0 _googlezone._tcp.local. [2m] PTR 7ae811b7-61f2-3416-eca5-883                                                                                                                                                              a6a1d18fb._googlezone._tcp.local., 7ae811b7-61f2-3416-eca5-883a6a1d18fb.local. (Cache flush) [2m] A 172.17.114.52, 7ae811b7-61                                                                                                                                                              f2-3416-eca5-883a6a1d18fb._googlezone._tcp.local. (Cache flush) [2m] SRV 7ae811b7-61f2-3416-eca5-883a6a1d18fb.local.:10001 610                                                                                                                                                               3, 7ae811b7-61f2-3416-eca5-883a6a1d18fb._googlezone._tcp.local. (Cache flush) [1h15m] TXT "id=85A57C757FBEACA4A8C5539E4D17F49                                                                                                                                                              E" "93d01926-c9e0-4458-b6bc-515a347c3ecc=0|Binnen" "e63b80d7-28e4-4ebf-9ba3-0ce60e73e8ff=0|Beneden" "f7934384-f50f-411d-8f15-d                                                                                                                                                              cf8ab39b5e2=0|Beneden-binnen" "__common_time__=0|0" (373)
17:40:29.208974 IP (tos 0x0, ttl 255, id 56327, offset 0, flags [DF], proto UDP (17), length 401)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 4/0/0 _googlezone._tcp.local. [2m] PTR 342ddd43-4372-2cdf-d284-401                                                                                                                                                              f9284f6b0._googlezone._tcp.local., 342ddd43-4372-2cdf-d284-401f9284f6b0.local. (Cache flush) [2m] A 172.17.114.18, 342ddd43-43                                                                                                                                                              72-2cdf-d284-401f9284f6b0._googlezone._tcp.local. (Cache flush) [2m] SRV 342ddd43-4372-2cdf-d284-401f9284f6b0.local.:10001 610                                                                                                                                                               123, 342ddd43-4372-2cdf-d284-401f9284f6b0._googlezone._tcp.local. (Cache flush) [1h15m] TXT "id=D44812348A098CDF225570FC4FBA7                                                                                                                                                              F1A" "93d01926-c9e0-4458-b6bc-515a347c3ecc=1|Binnen" "e63b80d7-28e4-4ebf-9ba3-0ce60e73e8ff=1|Beneden" "f7934384-f50f-411d-8f15                                                                                                                                                              -dcf8ab39b5e2=3|Beneden-binnen" "__common_time__=0|0" (373)
17:40:29.227260 IP (tos 0x0, ttl 255, id 56329, offset 0, flags [DF], proto UDP (17), length 68)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0 PTR (QM)? _googlezone._tcp.local. (40)
17:40:29.231059 IP (tos 0x0, ttl 255, id 56330, offset 0, flags [DF], proto UDP (17), length 105)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0 SRV (QM)? 5fd01e95-241c-a3d6-277f-62eb6326b954._googlezone._tcp.local. (7                                                                                                                                                              7)
17:40:29.272997 IP (tos 0x0, ttl 255, id 56331, offset 0, flags [DF], proto UDP (17), length 345)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 4/0/0 _googlezone._tcp.local. [2m] PTR 5fd01e95-241c-a3d6-277f-62e                                                                                                                                                              b6326b954._googlezone._tcp.local., 5fd01e95-241c-a3d6-277f-62eb6326b954.local. (Cache flush) [2m] A 172.17.114.24, 5fd01e95-24                                                                                                                                                              1c-a3d6-277f-62eb6326b954._googlezone._tcp.local. (Cache flush) [2m] SRV 5fd01e95-241c-a3d6-277f-62eb6326b954.local.:10001 610                                                                                                                                                               6, 5fd01e95-241c-a3d6-277f-62eb6326b954._googlezone._tcp.local. (Cache flush) [1h15m] TXT "id=6B0130740790B7044ED2EA5C3CB07A7                                                                                                                                                              B" "93d01926-c9e0-4458-b6bc-515a347c3ecc=0|Binnen" "b4389908-ab67-4809-a8b9-f02e3ccc711c=1|Boven" "__common_time__=0|0" (317)
17:40:29.276213 IP (tos 0x0, ttl 255, id 56332, offset 0, flags [DF], proto UDP (17), length 105)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0 SRV (QM)? 3777e026-f001-51e2-50f0-cf3c65a3883d._googlezone._tcp.local. (7                                                                                                                                                              7)
17:40:29.280981 IP (tos 0x0, ttl 255, id 56333, offset 0, flags [DF], proto UDP (17), length 105)
    10.1.0.1.5353 > 224.0.0.251.5353: [udp sum ok] 0 SRV (QM)? e8b58877-627a-8cea-281b-68f6f4a17d69._googlezone._tcp.local. (7                                                                                                                                                              7)
17:40:29.414152 IP6 (hlim 255, next-header UDP (17) payload length: 339) fe80::5ad5:aff:feb3:6be1.5353 > ff02::fb.5353: [udp s                                                                                                                                                              um ok] 0*- [0q] 5/0/0 gw-58d50ab36be1._coap._udp.local. (Cache flush) [5m] SRV TRADFRI-Gateway-58d50ab36be1.local.:5684 0 0, T                                                                                                                                                              RADFRI-Gateway-58d50ab36be1.local. (Cache flush) [2m] A 10.1.0.18, TRADFRI-Gateway-58d50ab36be1.local. (Cache flush) [2m] AAAA                                                                                                                                                               fe80::5ad5:aff:feb3:6be1, _coap._udp.local. [5m] PTR gw-58d50ab36be1._coap._udp.local., gw-58d50ab36be1._coap._udp.local. (Ca                                                                                                                                                              che flush) [5m] TXT "version=1.8.25" (331)
17:40:29.414311 IP (tos 0x0, ttl 255, id 79, offset 0, flags [DF], proto UDP (17), length 359)
    10.1.0.18.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 5/0/0 gw-58d50ab36be1._coap._udp.local. (Cache flush) [5m] SRV TR                                                                                                                                                              ADFRI-Gateway-58d50ab36be1.local.:5684 0 0, TRADFRI-Gateway-58d50ab36be1.local. (Cache flush) [2m] A 10.1.0.18, TRADFRI-Gatewa                                                                                                                                                              y-58d50ab36be1.local. (Cache flush) [2m] AAAA fe80::5ad5:aff:feb3:6be1, _coap._udp.local. [5m] PTR gw-58d50ab36be1._coap._udp.                                                                                                                                                              local., gw-58d50ab36be1._coap._udp.local. (Cache flush) [5m] TXT "version=1.8.25" (331)
17:40:30.414135 IP6 (hlim 255, next-header UDP (17) payload length: 339) fe80::5ad5:aff:feb3:6be1.5353 > ff02::fb.5353: [udp s                                                                                                                                                              um ok] 0*- [0q] 5/0/0 _coap._udp.local. [5m] PTR gw-58d50ab36be1._coap._udp.local., gw-58d50ab36be1._coap._udp.local. [5m] TXT                                                                                                                                                               "version=1.8.25", gw-58d50ab36be1._coap._udp.local. [2m] SRV TRADFRI-Gateway-58d50ab36be1.local.:5684 0 0, TRADFRI-Gateway-58                                                                                                                                                              d50ab36be1.local. [2m] A 10.1.0.18, TRADFRI-Gateway-58d50ab36be1.local. [2m] AAAA fe80::5ad5:aff:feb3:6be1 (331)
17:40:30.414299 IP (tos 0x0, ttl 255, id 80, offset 0, flags [DF], proto UDP (17), length 359)
    10.1.0.18.5353 > 224.0.0.251.5353: [udp sum ok] 0*- [0q] 5/0/0 _coap._udp.local. [5m] PTR gw-58d50ab36be1._coap._udp.local                                                                                                                                                              ., gw-58d50ab36be1._coap._udp.local. [5m] TXT "version=1.8.25", gw-58d50ab36be1._coap._udp.local. [2m] SRV TRADFRI-Gateway-58d                                                                                                                                                              50ab36be1.local.:5684 0 0, TRADFRI-Gateway-58d50ab36be1.local. [2m] A 10.1.0.18, TRADFRI-Gateway-58d50ab36be1.local. [2m] AAAA                                                                                                                                                               fe80::5ad5:aff:feb3:6be1 (331)
17:40:30.626869 IP (tos 0x0, ttl 128, id 81, offset 0, flags [none], proto TCP (6), length 313)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [P.], cksum 0xee49 (correct), seq 817:1090, ack 35481, win 7168, length 273: HTTP,                                                                                                                                                               length: 273
        GET /global/GW1.0/01.12.031/bin/10032198-2.2-TRADFRI-gateway-1.12.31.p.elf.sig.ota.signed HTTP/1.0
        User-Agent: HertzClient/1.0 (GW (1).(8).(25); Id ae5ff982-b2a5-431a-a307-88d4d284744b)
        Host: fw.ota.homesmart.ikea.net
        Range: bytes=18056-34439
        Connection: keep-alive

17:40:30.627283 IP (tos 0x0, ttl 255, id 82, offset 0, flags [DF], proto UDP (17), length 68)
    10.1.0.18.51325 > 10.1.0.1.53: [udp sum ok] 25827+ A? webhook.logentries.com. (40)
17:40:30.627512 IP (tos 0x0, ttl 255, id 83, offset 0, flags [DF], proto UDP (17), length 68)
    10.1.0.18.51325 > 8.8.8.8.53: [udp sum ok] 48352+ A? webhook.logentries.com. (40)
17:40:30.631810 IP (tos 0x0, ttl 64, id 55870, offset 0, flags [DF], proto UDP (17), length 164)
    10.1.0.1.53 > 10.1.0.18.51325: [udp sum ok] 25827 q: A? webhook.logentries.com. 6/0/0 webhook.logentries.com. [26s] A 54.1                                                                                                                                                              94.177.118, webhook.logentries.com. [26s] A 34.253.246.43, webhook.logentries.com. [26s] A 34.249.135.64, webhook.logentries.c                                                                                                                                                              om. [26s] A 52.19.32.171, webhook.logentries.com. [26s] A 34.255.232.56, webhook.logentries.com. [26s] A 52.49.133.235 (136)
17:40:30.632213 IP (tos 0x0, ttl 247, id 29171, offset 0, flags [none], proto TCP (6), length 40)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0xdb46 (correct), seq 35481, ack 1090, win 273, length 0
17:40:30.632959 IP (tos 0x80, ttl 124, id 13999, offset 0, flags [none], proto UDP (17), length 164)
    8.8.8.8.53 > 10.1.0.18.51325: [udp sum ok] 48352 q: A? webhook.logentries.com. 6/0/0 webhook.logentries.com. [16s] A 34.25                                                                                                                                                              3.246.43, webhook.logentries.com. [16s] A 54.194.177.118, webhook.logentries.com. [16s] A 52.19.32.171, webhook.logentries.com                                                                                                                                                              . [16s] A 52.49.133.235, webhook.logentries.com. [16s] A 34.255.232.56, webhook.logentries.com. [16s] A 34.249.135.64 (136)
17:40:30.633009 IP (tos 0x0, ttl 128, id 84, offset 0, flags [none], proto TCP (6), length 48)
    10.1.0.18.64368 > 54.194.177.118.443: Flags [S], cksum 0x64f7 (correct), seq 1474739402, win 7168, options [mss 1460,wscal                                                                                                                                                              e 0,eol], length 0
17:40:30.633288 IP (tos 0x0, ttl 255, id 85, offset 0, flags [none], proto ICMP (1), length 56)
    10.1.0.18 > 8.8.8.8: ICMP 10.1.0.18 udp port 51325 unreachable, length 36
        IP (tos 0x80, ttl 124, id 13999, offset 0, flags [none], proto UDP (17), length 164)
    8.8.8.8.53 > 10.1.0.18.51325: [|domain]
17:40:30.655022 IP (tos 0x0, ttl 238, id 0, offset 0, flags [DF], proto TCP (6), length 48)
    54.194.177.118.443 > 10.1.0.18.64368: Flags [S.], cksum 0x4d84 (correct), seq 1915705127, ack 1474739403, win 26883, optio                                                                                                                                                              ns [mss 1460,nop,wscale 8], length 0
17:40:30.655139 IP (tos 0x0, ttl 128, id 86, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.64368 > 54.194.177.118.443: Flags [.], cksum 0xc653 (correct), seq 1, ack 1, win 7168, length 0
17:40:30.655813 IP (tos 0x0, ttl 128, id 87, offset 0, flags [none], proto TCP (6), length 227)
    10.1.0.18.64368 > 54.194.177.118.443: Flags [P.], cksum 0x4967 (correct), seq 1:188, ack 1, win 7168, length 187
17:40:30.677730 IP (tos 0x0, ttl 238, id 15169, offset 0, flags [DF], proto TCP (6), length 40)
    54.194.177.118.443 > 10.1.0.18.64368: Flags [.], cksum 0xe12a (correct), seq 1, ack 188, win 110, length 0
17:40:30.677960 IP (tos 0x0, ttl 238, id 15170, offset 0, flags [DF], proto TCP (6), length 1500)
    54.194.177.118.443 > 10.1.0.18.64368: Flags [.], cksum 0x0b33 (correct), seq 1:1461, ack 188, win 110, length 1460
17:40:30.678175 IP (tos 0x0, ttl 238, id 15171, offset 0, flags [DF], proto TCP (6), length 1500)
    54.194.177.118.443 > 10.1.0.18.64368: Flags [.], cksum 0xc1d7 (correct), seq 1461:2921, ack 188, win 110, length 1460
17:40:30.678356 IP (tos 0x0, ttl 238, id 15172, offset 0, flags [DF], proto TCP (6), length 1216)
    54.194.177.118.443 > 10.1.0.18.64368: Flags [P.], cksum 0xf99d (correct), seq 2921:4097, ack 188, win 110, length 1176
17:40:30.678493 IP (tos 0x0, ttl 128, id 88, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.64368 > 54.194.177.118.443: Flags [.], cksum 0xba30 (correct), seq 188, ack 2921, win 7168, length 0
17:40:30.679286 IP (tos 0x0, ttl 238, id 15173, offset 0, flags [DF], proto TCP (6), length 1277)
    54.194.177.118.443 > 10.1.0.18.64368: Flags [P.], cksum 0xbad8 (correct), seq 4097:5334, ack 188, win 110, length 1237
17:40:30.679531 IP (tos 0x0, ttl 128, id 89, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.64368 > 54.194.177.118.443: Flags [.], cksum 0xb0c3 (correct), seq 188, ack 5334, win 7168, length 0
17:40:30.894084 IP (tos 0x0, ttl 128, id 90, offset 0, flags [none], proto TCP (6), length 115)
    10.1.0.18.64368 > 54.194.177.118.443: Flags [P.], cksum 0x12ed (correct), seq 188:263, ack 5334, win 7168, length 75
17:40:30.895288 IP (tos 0x0, ttl 128, id 91, offset 0, flags [none], proto TCP (6), length 46)
    10.1.0.18.64368 > 54.194.177.118.443: Flags [P.], cksum 0x9866 (correct), seq 263:269, ack 5334, win 7168, length 6
17:40:30.895738 IP (tos 0x0, ttl 128, id 92, offset 0, flags [none], proto TCP (6), length 85)
    10.1.0.18.64368 > 54.194.177.118.443: Flags [P.], cksum 0x79b0 (correct), seq 269:314, ack 5334, win 7168, length 45
17:40:30.917318 IP (tos 0x0, ttl 238, id 15174, offset 0, flags [DF], proto TCP (6), length 40)
    54.194.177.118.443 > 10.1.0.18.64368: Flags [.], cksum 0xcc04 (correct), seq 5334, ack 269, win 110, length 0
17:40:30.917747 IP (tos 0x0, ttl 238, id 15175, offset 0, flags [DF], proto TCP (6), length 91)
    54.194.177.118.443 > 10.1.0.18.64368: Flags [P.], cksum 0x6ef5 (correct), seq 5334:5385, ack 314, win 110, length 51
17:40:30.918946 IP (tos 0x0, ttl 128, id 93, offset 0, flags [none], proto TCP (6), length 434)
    10.1.0.18.64368 > 54.194.177.118.443: Flags [P.], cksum 0x3ac2 (correct), seq 314:708, ack 5385, win 7168, length 394
17:40:30.941537 IP (tos 0x0, ttl 238, id 15176, offset 0, flags [DF], proto TCP (6), length 239)
    54.194.177.118.443 > 10.1.0.18.64368: Flags [P.], cksum 0xa52f (correct), seq 5385:5584, ack 708, win 114, length 199
17:40:30.941691 IP (tos 0x0, ttl 128, id 94, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.64368 > 54.194.177.118.443: Flags [.], cksum 0xadc1 (correct), seq 708, ack 5584, win 7168, length 0
17:40:30.942744 IP (tos 0x0, ttl 128, id 95, offset 0, flags [none], proto TCP (6), length 437)
    10.1.0.18.64368 > 54.194.177.118.443: Flags [P.], cksum 0xae4f (correct), seq 708:1105, ack 5584, win 7168, length 397
17:40:30.965126 IP (tos 0x0, ttl 238, id 15177, offset 0, flags [DF], proto TCP (6), length 239)
    54.194.177.118.443 > 10.1.0.18.64368: Flags [P.], cksum 0x67ac (correct), seq 5584:5783, ack 1105, win 118, length 199
17:40:30.966202 IP (tos 0x0, ttl 128, id 96, offset 0, flags [none], proto TCP (6), length 437)
    10.1.0.18.64368 > 54.194.177.118.443: Flags [P.], cksum 0x08c8 (correct), seq 1105:1502, ack 5783, win 7168, length 397
17:40:30.988931 IP (tos 0x0, ttl 238, id 15178, offset 0, flags [DF], proto TCP (6), length 239)
    54.194.177.118.443 > 10.1.0.18.64368: Flags [P.], cksum 0xecfd (correct), seq 5783:5982, ack 1502, win 122, length 199
17:40:30.989081 IP (tos 0x0, ttl 128, id 97, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.64368 > 54.194.177.118.443: Flags [.], cksum 0xa919 (correct), seq 1502, ack 5982, win 7168, length 0
17:40:30.990027 IP (tos 0x0, ttl 128, id 98, offset 0, flags [none], proto TCP (6), length 437)
    10.1.0.18.64368 > 54.194.177.118.443: Flags [P.], cksum 0xe75e (correct), seq 1502:1899, ack 5982, win 7168, length 397
17:40:31.010607 IP (tos 0x0, ttl 247, id 29192, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x00ef (correct), seq 35481:36931, ack 1090, win 273, length 1450: HTTP                                                                                                                                                              , length: 1450
        HTTP/1.1 206 Partial Content
        Content-Type: application/octet-stream
        Content-Length: 16384
        Connection: keep-alive
        x-amz-id-2: z8UHmX5DhLSMUklEbnGKSrTxUrCup9adtoQAGBh6vWBZOdIm/PBjzD1XY7nGlm+IMPL4P96pbcs=
        x-amz-request-id: D32529443F17BFEE
        x-amz-replication-status: COMPLETED
        Last-Modified: Tue, 24 Nov 2020 11:58:35 GMT
        x-amz-version-id: Q7SCltPeHFFpYmqCkNIdy.Hws_ZUJEhk
        Accept-Ranges: bytes
        Server: AmazonS3
        Date: Mon, 14 Dec 2020 14:40:00 GMT
        ETag: "6504c28dfcdebd0a5dd533ef250f1dfc"
        Content-Range: bytes 18056-34439/829224
        X-Cache: Hit from cloudfront
        Via: 1.1 d143bdfb7cce4cf7ec0bcf9ec13e5915.cloudfront.net (CloudFront)
        X-Amz-Cf-Pop: AMS1-C1
        X-Amz-Cf-Id: JAPL6orxM6z1ogyZLFDxY8El4rCUR4Q1tWSGVcYKB2lx67AWJAbtww==

17:40:31.010791 IP (tos 0x0, ttl 247, id 29193, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0xf005 (correct), seq 36931:38381, ack 1090, win 273, length 1450: HTT                                                                                                                                                              P
17:40:31.011003 IP (tos 0x0, ttl 247, id 29194, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x93fe (correct), seq 38381:39831, ack 1090, win 273, length 1450: HTTP
17:40:31.011185 IP (tos 0x0, ttl 247, id 29195, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0x2de9 (correct), seq 39831:41281, ack 1090, win 273, length 1450: HTT                                                                                                                                                              P
17:40:31.011234 IP (tos 0x0, ttl 128, id 99, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0xbaad (correct), seq 1090, ack 38381, win 5718, length 0
17:40:31.011633 IP (tos 0x0, ttl 128, id 100, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0xa9af (correct), seq 1090, ack 41281, win 7168, length 0
17:40:31.011833 IP (tos 0x0, ttl 128, id 101, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0xa9af (correct), seq 1090, ack 41281, win 7168, length 0
17:40:31.013445 IP (tos 0x0, ttl 128, id 102, offset 0, flags [none], proto TCP (6), length 437)
    10.1.0.18.64368 > 54.194.177.118.443: Flags [P.], cksum 0x74b0 (correct), seq 1899:2296, ack 6181, win 7168, length 397
17:40:31.016514 IP (tos 0x0, ttl 247, id 29196, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x247d (correct), seq 41281:42731, ack 1090, win 273, length 1450: HTTP
17:40:31.016698 IP (tos 0x0, ttl 247, id 29197, offset 0, flags [none], proto TCP (6), length 1408)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0x7378 (correct), seq 42731:44099, ack 1090, win 273, length 1368: HTT                                                                                                                                                              P
17:40:31.016888 IP (tos 0x0, ttl 247, id 29198, offset 0, flags [none], proto TCP (6), length 122)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x6532 (correct), seq 44099:44181, ack 1090, win 273, length 82: HTTP
17:40:31.017061 IP (tos 0x0, ttl 247, id 29199, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x2c7b (correct), seq 44181:45631, ack 1090, win 273, length 1450: HTTP
17:40:31.017110 IP (tos 0x0, ttl 128, id 103, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x9ead (correct), seq 1090, ack 44099, win 7168, length 0
17:40:31.017400 IP (tos 0x0, ttl 247, id 29200, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0x00d4 (correct), seq 45631:47081, ack 1090, win 273, length 1450: HTT                                                                                                                                                              P
17:40:31.017457 IP (tos 0x0, ttl 128, id 104, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x98b1 (correct), seq 1090, ack 45631, win 7168, length 0
17:40:31.022413 IP (tos 0x0, ttl 247, id 29201, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0xaf0d (correct), seq 47081:48531, ack 1090, win 273, length 1450: HTTP
17:40:31.022588 IP (tos 0x0, ttl 247, id 29202, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0x2707 (correct), seq 48531:49981, ack 1090, win 273, length 1450: HTT                                                                                                                                                              P
17:40:31.022813 IP (tos 0x0, ttl 247, id 29203, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x594a (correct), seq 49981:51431, ack 1090, win 273, length 1450: HTTP
17:40:31.022994 IP (tos 0x0, ttl 247, id 29204, offset 0, flags [none], proto TCP (6), length 1209)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0x6716 (correct), seq 51431:52600, ack 1090, win 273, length 1169: HTT                                                                                                                                                              P
17:40:31.023042 IP (tos 0x0, ttl 128, id 105, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x8d5d (correct), seq 1090, ack 48531, win 7168, length 0
17:40:31.023221 IP (tos 0x0, ttl 128, id 106, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x8209 (correct), seq 1090, ack 51431, win 7168, length 0
17:40:31.036588 IP (tos 0x0, ttl 238, id 15180, offset 0, flags [DF], proto TCP (6), length 239)
    54.194.177.118.443 > 10.1.0.18.64368: Flags [P.], cksum 0xc733 (correct), seq 6181:6380, ack 2296, win 131, length 199
17:40:31.036736 IP (tos 0x0, ttl 128, id 107, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.64368 > 54.194.177.118.443: Flags [.], cksum 0xa471 (correct), seq 2296, ack 6380, win 7168, length 0
17:40:31.129069 IP (tos 0x0, ttl 128, id 108, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x7d78 (correct), seq 1090, ack 52600, win 7168, length 0
17:40:31.820998 IP (tos 0x0, ttl 128, id 109, offset 0, flags [none], proto TCP (6), length 313)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [P.], cksum 0xaa63 (correct), seq 1090:1363, ack 52600, win 7168, length 273: HTTP                                                                                                                                                              , length: 273
        GET /global/GW1.0/01.12.031/bin/10032198-2.2-TRADFRI-gateway-1.12.31.p.elf.sig.ota.signed HTTP/1.0
        User-Agent: HertzClient/1.0 (GW (1).(8).(25); Id ae5ff982-b2a5-431a-a307-88d4d284744b)
        Host: fw.ota.homesmart.ikea.net
        Range: bytes=34440-50823
        Connection: keep-alive

17:40:31.822131 IP (tos 0x0, ttl 128, id 110, offset 0, flags [none], proto TCP (6), length 510)
    10.1.0.18.64368 > 54.194.177.118.443: Flags [P.], cksum 0x12b0 (correct), seq 2296:2766, ack 6380, win 7168, length 470
17:40:31.826460 IP (tos 0x0, ttl 247, id 29270, offset 0, flags [none], proto TCP (6), length 40)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x9752 (correct), seq 52600, ack 1363, win 277, length 0
17:40:31.844563 IP (tos 0x0, ttl 238, id 15181, offset 0, flags [DF], proto TCP (6), length 239)
    54.194.177.118.443 > 10.1.0.18.64368: Flags [P.], cksum 0xdf98 (correct), seq 6380:6579, ack 2766, win 135, length 199
17:40:31.845648 IP (tos 0x0, ttl 128, id 111, offset 0, flags [none], proto TCP (6), length 435)
    10.1.0.18.64368 > 54.194.177.118.443: Flags [P.], cksum 0x4631 (correct), seq 2766:3161, ack 6579, win 7168, length 395
17:40:31.867956 IP (tos 0x0, ttl 238, id 15182, offset 0, flags [DF], proto TCP (6), length 239)
    54.194.177.118.443 > 10.1.0.18.64368: Flags [P.], cksum 0x6cf7 (correct), seq 6579:6778, ack 3161, win 139, length 199
17:40:31.868106 IP (tos 0x0, ttl 128, id 112, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.64368 > 54.194.177.118.443: Flags [.], cksum 0x9f82 (correct), seq 3161, ack 6778, win 7168, length 0
17:40:31.869156 IP (tos 0x0, ttl 128, id 113, offset 0, flags [none], proto TCP (6), length 434)
    10.1.0.18.64368 > 54.194.177.118.443: Flags [P.], cksum 0xf74f (correct), seq 3161:3555, ack 6778, win 7168, length 394
17:40:31.891544 IP (tos 0x0, ttl 238, id 15183, offset 0, flags [DF], proto TCP (6), length 239)
    54.194.177.118.443 > 10.1.0.18.64368: Flags [P.], cksum 0xb465 (correct), seq 6778:6977, ack 3555, win 143, length 199
17:40:31.892698 IP (tos 0x0, ttl 128, id 114, offset 0, flags [none], proto TCP (6), length 436)
    10.1.0.18.64368 > 54.194.177.118.443: Flags [P.], cksum 0x5abd (correct), seq 3555:3951, ack 6977, win 7168, length 396
17:40:31.915290 IP (tos 0x0, ttl 238, id 15184, offset 0, flags [DF], proto TCP (6), length 239)
    54.194.177.118.443 > 10.1.0.18.64368: Flags [P.], cksum 0x7a6f (correct), seq 6977:7176, ack 3951, win 147, length 199
17:40:31.915433 IP (tos 0x0, ttl 128, id 115, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.64368 > 54.194.177.118.443: Flags [.], cksum 0x9ade (correct), seq 3951, ack 7176, win 7168, length 0
17:40:31.916459 IP (tos 0x0, ttl 128, id 116, offset 0, flags [none], proto TCP (6), length 436)
    10.1.0.18.64368 > 54.194.177.118.443: Flags [P.], cksum 0x84fa (correct), seq 3951:4347, ack 7176, win 7168, length 396
17:40:31.938994 IP (tos 0x0, ttl 238, id 15185, offset 0, flags [DF], proto TCP (6), length 239)
    54.194.177.118.443 > 10.1.0.18.64368: Flags [P.], cksum 0x3a6d (correct), seq 7176:7375, ack 4347, win 152, length 199
17:40:31.939346 IP (tos 0x0, ttl 128, id 117, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.64368 > 54.194.177.118.443: Flags [F.], cksum 0x988a (correct), seq 4347, ack 7375, win 7168, length 0
17:40:31.961471 IP (tos 0x0, ttl 238, id 15186, offset 0, flags [DF], proto TCP (6), length 71)
    54.194.177.118.443 > 10.1.0.18.64368: Flags [P.], cksum 0x4d21 (correct), seq 7375:7406, ack 4348, win 152, length 31
17:40:31.961643 IP (tos 0x0, ttl 238, id 15187, offset 0, flags [DF], proto TCP (6), length 40)
    54.194.177.118.443 > 10.1.0.18.64368: Flags [F.], cksum 0xb3d2 (correct), seq 7406, ack 4348, win 152, length 0
17:40:31.961746 IP (tos 0x0, ttl 128, id 118, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.64368 > 54.194.177.118.443: Flags [.], cksum 0x9889 (correct), seq 4348, ack 7407, win 7137, length 0
17:40:32.200779 IP (tos 0x0, ttl 247, id 29282, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0xdc75 (correct), seq 52600:54050, ack 1363, win 277, length 1450: HTTP                                                                                                                                                              , length: 1450
        HTTP/1.1 206 Partial Content
        Content-Type: application/octet-stream
        Content-Length: 16384
        Connection: keep-alive
        x-amz-id-2: z8UHmX5DhLSMUklEbnGKSrTxUrCup9adtoQAGBh6vWBZOdIm/PBjzD1XY7nGlm+IMPL4P96pbcs=
        x-amz-request-id: D32529443F17BFEE
        x-amz-replication-status: COMPLETED
        Last-Modified: Tue, 24 Nov 2020 11:58:35 GMT
        x-amz-version-id: Q7SCltPeHFFpYmqCkNIdy.Hws_ZUJEhk
        Accept-Ranges: bytes
        Server: AmazonS3
        Date: Mon, 14 Dec 2020 14:40:00 GMT
        ETag: "6504c28dfcdebd0a5dd533ef250f1dfc"
        Content-Range: bytes 34440-50823/829224
        X-Cache: Hit from cloudfront
        Via: 1.1 d143bdfb7cce4cf7ec0bcf9ec13e5915.cloudfront.net (CloudFront)
        X-Amz-Cf-Pop: AMS1-C1
        X-Amz-Cf-Id: QYa7UCpxp4xoH8pktTs1ssoZrR1J7I5mGh5GTBO8AQPalAM92XFluQ==

17:40:32.200960 IP (tos 0x0, ttl 247, id 29283, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0x0189 (correct), seq 54050:55500, ack 1363, win 277, length 1450: HTT                                                                                                                                                              P
17:40:32.201129 IP (tos 0x0, ttl 247, id 29284, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0xc633 (correct), seq 55500:56950, ack 1363, win 277, length 1450: HTTP
17:40:32.201281 IP (tos 0x0, ttl 247, id 29285, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0x4dee (correct), seq 56950:58400, ack 1363, win 277, length 1450: HTT                                                                                                                                                              P
17:40:32.201322 IP (tos 0x0, ttl 128, id 119, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x76bd (correct), seq 1363, ack 54050, win 7168, length 0
17:40:32.201453 IP (tos 0x0, ttl 128, id 120, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x6b69 (correct), seq 1363, ack 56950, win 7168, length 0
17:40:32.206653 IP (tos 0x0, ttl 247, id 29286, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x5231 (correct), seq 58400:59850, ack 1363, win 277, length 1450: HTTP
17:40:32.206825 IP (tos 0x0, ttl 247, id 29287, offset 0, flags [none], proto TCP (6), length 1408)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0xed8d (correct), seq 59850:61218, ack 1363, win 277, length 1368: HTT                                                                                                                                                              P
17:40:32.207005 IP (tos 0x0, ttl 247, id 29288, offset 0, flags [none], proto TCP (6), length 122)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x84f7 (correct), seq 61218:61300, ack 1363, win 277, length 82: HTTP
17:40:32.207163 IP (tos 0x0, ttl 247, id 29289, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x49a4 (correct), seq 61300:62750, ack 1363, win 277, length 1450: HTTP
17:40:32.207207 IP (tos 0x0, ttl 128, id 121, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x6015 (correct), seq 1363, ack 59850, win 7168, length 0
17:40:32.207463 IP (tos 0x0, ttl 247, id 29290, offset 0, flags [none], proto TCP (6), length 1408)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0xc463 (correct), seq 62750:64118, ack 1363, win 277, length 1368: HTT                                                                                                                                                              P
17:40:32.207507 IP (tos 0x0, ttl 128, id 122, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x5a6b (correct), seq 1363, ack 61300, win 7168, length 0
17:40:32.207880 IP (tos 0x0, ttl 128, id 123, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x4f69 (correct), seq 1363, ack 64118, win 7168, length 0
17:40:32.212480 IP (tos 0x0, ttl 247, id 29291, offset 0, flags [none], proto TCP (6), length 122)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0xda52 (correct), seq 64118:64200, ack 1363, win 277, length 82: HTTP
17:40:32.212651 IP (tos 0x0, ttl 247, id 29292, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0xb387 (correct), seq 64200:65650, ack 1363, win 277, length 1450: HTTP
17:40:32.212828 IP (tos 0x0, ttl 247, id 29293, offset 0, flags [none], proto TCP (6), length 1408)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0xf061 (correct), seq 65650:67018, ack 1363, win 277, length 1368: HTT                                                                                                                                                              P
17:40:32.212888 IP (tos 0x0, ttl 128, id 124, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x496d (correct), seq 1363, ack 65650, win 7168, length 0
17:40:32.214436 IP (tos 0x0, ttl 247, id 29294, offset 0, flags [none], proto TCP (6), length 122)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0xab06 (correct), seq 67018:67100, ack 1363, win 277, length 82: HTTP
17:40:32.214546 IP (tos 0x0, ttl 128, id 125, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x43c3 (correct), seq 1363, ack 67100, win 7168, length 0
17:40:32.214861 IP (tos 0x0, ttl 247, id 29295, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x0307 (correct), seq 67100:68550, ack 1363, win 277, length 1450: HTTP
17:40:32.215043 IP (tos 0x0, ttl 247, id 29296, offset 0, flags [none], proto TCP (6), length 1209)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0xce8e (correct), seq 68550:69719, ack 1363, win 277, length 1169: HTT                                                                                                                                                              P
17:40:32.215265 IP (tos 0x0, ttl 128, id 126, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x3988 (correct), seq 1363, ack 69719, win 7168, length 0
17:40:33.008239 IP (tos 0x0, ttl 128, id 127, offset 0, flags [none], proto TCP (6), length 313)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [P.], cksum 0x5d74 (correct), seq 1363:1636, ack 69719, win 7168, length 273: HTTP                                                                                                                                                              , length: 273
        GET /global/GW1.0/01.12.031/bin/10032198-2.2-TRADFRI-gateway-1.12.31.p.elf.sig.ota.signed HTTP/1.0
        User-Agent: HertzClient/1.0 (GW (1).(8).(25); Id ae5ff982-b2a5-431a-a307-88d4d284744b)
        Host: fw.ota.homesmart.ikea.net
        Range: bytes=50824-67207
        Connection: keep-alive

17:40:33.013779 IP (tos 0x0, ttl 247, id 29377, offset 0, flags [none], proto TCP (6), length 40)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x535d (correct), seq 69719, ack 1636, win 282, length 0
17:40:33.467467 IP (tos 0x0, ttl 247, id 29408, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0xe7ba (correct), seq 69719:71169, ack 1636, win 282, length 1450: HTTP                                                                                                                                                              , length: 1450
        HTTP/1.1 206 Partial Content
        Content-Type: application/octet-stream
        Content-Length: 16384
        Connection: keep-alive
        x-amz-id-2: z8UHmX5DhLSMUklEbnGKSrTxUrCup9adtoQAGBh6vWBZOdIm/PBjzD1XY7nGlm+IMPL4P96pbcs=
        x-amz-request-id: D32529443F17BFEE
        x-amz-replication-status: COMPLETED
        Last-Modified: Tue, 24 Nov 2020 11:58:35 GMT
        x-amz-version-id: Q7SCltPeHFFpYmqCkNIdy.Hws_ZUJEhk
        Accept-Ranges: bytes
        Server: AmazonS3
        Date: Mon, 14 Dec 2020 14:40:00 GMT
        ETag: "6504c28dfcdebd0a5dd533ef250f1dfc"
        Content-Range: bytes 50824-67207/829224
        X-Cache: Hit from cloudfront
        Via: 1.1 d143bdfb7cce4cf7ec0bcf9ec13e5915.cloudfront.net (CloudFront)
        X-Amz-Cf-Pop: AMS1-C1
        X-Amz-Cf-Id: irjrF-WsW_MqZ6Q5P29rQmidwNZz0UDsRE-PAKGPu5pGexr_wvHAYA==

17:40:33.467627 IP (tos 0x0, ttl 247, id 29409, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0x2d5e (correct), seq 71169:72619, ack 1636, win 282, length 1450: HTT                                                                                                                                                              P
17:40:33.467897 IP (tos 0x0, ttl 128, id 128, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x32cd (correct), seq 1636, ack 72619, win 5718, length 0
17:40:33.468359 IP (tos 0x0, ttl 247, id 29410, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0xbcd0 (correct), seq 72619:74069, ack 1636, win 282, length 1450: HTTP
17:40:33.468481 IP (tos 0x0, ttl 247, id 29411, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0xf546 (correct), seq 74069:75519, ack 1636, win 282, length 1450: HTT                                                                                                                                                              P
17:40:33.468737 IP (tos 0x0, ttl 128, id 129, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x21cf (correct), seq 1636, ack 75519, win 7168, length 0
17:40:33.468927 IP (tos 0x0, ttl 128, id 130, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x21cf (correct), seq 1636, ack 75519, win 7168, length 0
17:40:33.473110 IP (tos 0x0, ttl 247, id 29412, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x6656 (correct), seq 75519:76969, ack 1636, win 282, length 1450: HTTP
17:40:33.473242 IP (tos 0x0, ttl 247, id 29413, offset 0, flags [none], proto TCP (6), length 1408)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0xa152 (correct), seq 76969:78337, ack 1636, win 282, length 1368: HTT                                                                                                                                                              P
17:40:33.473490 IP (tos 0x0, ttl 128, id 131, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x16cd (correct), seq 1636, ack 78337, win 7168, length 0
17:40:33.478976 IP (tos 0x0, ttl 247, id 29417, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0xc1bb (correct), seq 81319:82769, ack 1636, win 282, length 1450: HTTP
17:40:33.479138 IP (tos 0x0, ttl 247, id 29418, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0xc98e (correct), seq 82769:84219, ack 1636, win 282, length 1450: HTT                                                                                                                                                              P
17:40:33.479251 IP (tos 0x0, ttl 128, id 133, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x057d (correct), seq 1636, ack 82769, win 7168, length 0
17:40:33.479678 IP (tos 0x0, ttl 247, id 29419, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x55c2 (correct), seq 84219:85669, ack 1636, win 282, length 1450: HTTP
17:40:33.479804 IP (tos 0x0, ttl 247, id 29420, offset 0, flags [none], proto TCP (6), length 1209)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0xbe54 (correct), seq 85669:86838, ack 1636, win 282, length 1169: HTT                                                                                                                                                              P
17:40:33.480023 IP (tos 0x0, ttl 128, id 134, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0xfa28 (correct), seq 1636, ack 85669, win 7168, length 0
17:40:33.629077 IP (tos 0x0, ttl 128, id 135, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0xf597 (correct), seq 1636, ack 86838, win 7168, length 0
17:40:34.273508 IP (tos 0x0, ttl 128, id 136, offset 0, flags [none], proto TCP (6), length 313)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [P.], cksum 0x1b7a (correct), seq 1636:1909, ack 86838, win 7168, length 273: HTTP                                                                                                                                                              , length: 273
        GET /global/GW1.0/01.12.031/bin/10032198-2.2-TRADFRI-gateway-1.12.31.p.elf.sig.ota.signed HTTP/1.0
        User-Agent: HertzClient/1.0 (GW (1).(8).(25); Id ae5ff982-b2a5-431a-a307-88d4d284744b)
        Host: fw.ota.homesmart.ikea.net
        Range: bytes=67208-83591
        Connection: keep-alive

17:40:34.278703 IP (tos 0x0, ttl 247, id 29476, offset 0, flags [none], proto TCP (6), length 40)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x0f69 (correct), seq 86838, ack 1909, win 286, length 0
17:40:34.642380 IP (tos 0x0, ttl 247, id 29501, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0xc1f8 (correct), seq 86838:88288, ack 1909, win 286, length 1450: HTTP                                                                                                                                                              , length: 1450
        HTTP/1.1 206 Partial Content
        Content-Type: application/octet-stream
        Content-Length: 16384
        Connection: keep-alive
        x-amz-id-2: z8UHmX5DhLSMUklEbnGKSrTxUrCup9adtoQAGBh6vWBZOdIm/PBjzD1XY7nGlm+IMPL4P96pbcs=
        x-amz-request-id: D32529443F17BFEE
        x-amz-replication-status: COMPLETED
        Last-Modified: Tue, 24 Nov 2020 11:58:35 GMT
        x-amz-version-id: Q7SCltPeHFFpYmqCkNIdy.Hws_ZUJEhk
        Accept-Ranges: bytes
        Server: AmazonS3
        Date: Mon, 14 Dec 2020 14:40:00 GMT
        ETag: "6504c28dfcdebd0a5dd533ef250f1dfc"
        Content-Range: bytes 67208-83591/829224
        X-Cache: Hit from cloudfront
        Via: 1.1 d143bdfb7cce4cf7ec0bcf9ec13e5915.cloudfront.net (CloudFront)
        X-Amz-Cf-Pop: AMS1-C1
        X-Amz-Cf-Id: Kex3E7XdmUY4oOv-dTiBmd4KVO4XD_5PcWy1pnBOt0-4ol0dCKtfEw==

17:40:34.642542 IP (tos 0x0, ttl 247, id 29502, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0x0fd6 (correct), seq 88288:89738, ack 1909, win 286, length 1450: HTT                                                                                                                                                              P
17:40:34.642664 IP (tos 0x0, ttl 128, id 137, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0xeedc (correct), seq 1909, ack 88288, win 7168, length 0
17:40:34.643459 IP (tos 0x0, ttl 247, id 29503, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x8ab5 (correct), seq 89738:91188, ack 1909, win 286, length 1450: HTTP
17:40:34.643594 IP (tos 0x0, ttl 247, id 29504, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0xd1e1 (correct), seq 91188:92638, ack 1909, win 286, length 1450: HTT                                                                                                                                                              P
17:40:34.643715 IP (tos 0x0, ttl 128, id 138, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0xe388 (correct), seq 1909, ack 91188, win 7168, length 0
17:40:34.647862 IP (tos 0x0, ttl 247, id 29505, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0xd5d0 (correct), seq 92638:94088, ack 1909, win 286, length 1450: HTTP
17:40:34.647997 IP (tos 0x0, ttl 247, id 29506, offset 0, flags [none], proto TCP (6), length 1408)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0x7775 (correct), seq 94088:95456, ack 1909, win 286, length 1368: HTT                                                                                                                                                              P
17:40:34.648952 IP (tos 0x0, ttl 247, id 29507, offset 0, flags [none], proto TCP (6), length 122)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x4136 (correct), seq 95456:95538, ack 1909, win 286, length 82: HTTP
17:40:34.653404 IP (tos 0x0, ttl 247, id 29510, offset 0, flags [none], proto TCP (6), length 122)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0x17b6 (correct), seq 98356:98438, ack 1909, win 286, length 82: HTTP
17:40:34.653583 IP (tos 0x0, ttl 247, id 29511, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x56dd (correct), seq 98438:99888, ack 1909, win 286, length 1450: HTTP
17:40:34.653722 IP (tos 0x0, ttl 247, id 29512, offset 0, flags [none], proto TCP (6), length 1408)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0xabde (correct), seq 99888:101256, ack 1909, win 286, length 1368: HT                                                                                                                                                              TP
17:40:34.653959 IP (tos 0x0, ttl 128, id 142, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0xc18c (correct), seq 1909, ack 99888, win 7168, length 0
17:40:34.654936 IP (tos 0x0, ttl 247, id 29513, offset 0, flags [none], proto TCP (6), length 122)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x0389 (correct), seq 101256:101338, ack 1909, win 286, length 82: HTTP
17:40:34.655106 IP (tos 0x0, ttl 247, id 29514, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0xf6b7 (correct), seq 101338:102788, ack 1909, win 286, length 1450: HT                                                                                                                                                              TP
17:40:34.655278 IP (tos 0x0, ttl 247, id 29515, offset 0, flags [none], proto TCP (6), length 1209)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0x5075 (correct), seq 102788:103957, ack 1909, win 286, length 1169: H                                                                                                                                                              TTP
17:40:35.448229 IP (tos 0x0, ttl 128, id 145, offset 0, flags [none], proto TCP (6), length 313)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [P.], cksum 0xcf80 (correct), seq 1909:2182, ack 103957, win 7168, length 273: HTT                                                                                                                                                              P, length: 273
        GET /global/GW1.0/01.12.031/bin/10032198-2.2-TRADFRI-gateway-1.12.31.p.elf.sig.ota.signed HTTP/1.0
        User-Agent: HertzClient/1.0 (GW (1).(8).(25); Id ae5ff982-b2a5-431a-a307-88d4d284744b)
        Host: fw.ota.homesmart.ikea.net
        Range: bytes=83592-99975
        Connection: keep-alive

17:40:35.453421 IP (tos 0x0, ttl 247, id 29529, offset 0, flags [none], proto TCP (6), length 40)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0xcb74 (correct), seq 103957, ack 2182, win 290, length 0
17:40:35.821850 IP (tos 0x0, ttl 247, id 29577, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x30cd (correct), seq 103957:105407, ack 2182, win 290, length 1450: HT                                                                                                                                                              TP, length: 1450
        HTTP/1.1 206 Partial Content
        Content-Type: application/octet-stream
        Content-Length: 16384
        Connection: keep-alive
        x-amz-id-2: z8UHmX5DhLSMUklEbnGKSrTxUrCup9adtoQAGBh6vWBZOdIm/PBjzD1XY7nGlm+IMPL4P96pbcs=
        x-amz-request-id: D32529443F17BFEE
        x-amz-replication-status: COMPLETED
        Last-Modified: Tue, 24 Nov 2020 11:58:35 GMT
        x-amz-version-id: Q7SCltPeHFFpYmqCkNIdy.Hws_ZUJEhk
        Accept-Ranges: bytes
        Server: AmazonS3
        Date: Mon, 14 Dec 2020 14:40:00 GMT
        ETag: "6504c28dfcdebd0a5dd533ef250f1dfc"
        Content-Range: bytes 83592-99975/829224
        X-Cache: Hit from cloudfront
        Via: 1.1 d143bdfb7cce4cf7ec0bcf9ec13e5915.cloudfront.net (CloudFront)
        X-Amz-Cf-Pop: AMS1-C1
        X-Amz-Cf-Id: 8E9JzZZCu8ahr9WpxYnxmpUmOm3ZY_pN23tgCgw0b3yIdu2SaSnf_A==

17:40:35.822071 IP (tos 0x0, ttl 247, id 29578, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0xfdf6 (correct), seq 105407:106857, ack 2182, win 290, length 1450: H                                                                                                                                                              TTP
17:40:35.822517 IP (tos 0x0, ttl 128, id 146, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0xaaec (correct), seq 2182, ack 106857, win 5718, length 0
17:40:35.822853 IP (tos 0x0, ttl 247, id 29579, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x623b (correct), seq 106857:108307, ack 2182, win 290, length 1450: HT                                                                                                                                                              TP
17:40:35.823030 IP (tos 0x0, ttl 247, id 29580, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0x0540 (correct), seq 108307:109757, ack 2182, win 290, length 1450: H                                                                                                                                                              TTP
17:40:35.823291 IP (tos 0x0, ttl 128, id 147, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x99ee (correct), seq 2182, ack 109757, win 7168, length 0
17:40:35.823515 IP (tos 0x0, ttl 128, id 148, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x99ee (correct), seq 2182, ack 109757, win 7168, length 0
17:40:35.827865 IP (tos 0x0, ttl 247, id 29581, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x2869 (correct), seq 109757:111207, ack 2182, win 290, length 1450: HT                                                                                                                                                              TP
17:40:35.828087 IP (tos 0x0, ttl 247, id 29582, offset 0, flags [none], proto TCP (6), length 1408)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0xd5f9 (correct), seq 111207:112575, ack 2182, win 290, length 1368: H                                                                                                                                                              TTP
17:40:35.828344 IP (tos 0x0, ttl 128, id 149, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x8eec (correct), seq 2182, ack 112575, win 7168, length 0
17:40:35.828926 IP (tos 0x0, ttl 247, id 29583, offset 0, flags [none], proto TCP (6), length 122)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x5386 (correct), seq 112575:112657, ack 2182, win 290, length 82: HTTP
17:40:35.829108 IP (tos 0x0, ttl 247, id 29584, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x026c (correct), seq 112657:114107, ack 2182, win 290, length 1450: HT                                                                                                                                                              TP
17:40:35.829288 IP (tos 0x0, ttl 247, id 29585, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0xc8b9 (correct), seq 114107:115557, ack 2182, win 290, length 1450: H                                                                                                                                                              TTP
17:40:35.829353 IP (tos 0x0, ttl 128, id 150, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x88f0 (correct), seq 2182, ack 114107, win 7168, length 0
17:40:35.833787 IP (tos 0x0, ttl 247, id 29586, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x1130 (correct), seq 115557:117007, ack 2182, win 290, length 1450: HT                                                                                                                                                              TP
17:40:35.833967 IP (tos 0x0, ttl 247, id 29587, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0x372d (correct), seq 117007:118457, ack 2182, win 290, length 1450: H                                                                                                                                                              TTP
17:40:35.834027 IP (tos 0x0, ttl 128, id 151, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x7d9c (correct), seq 2182, ack 117007, win 7168, length 0
17:40:36.029084 IP (tos 0x0, ttl 128, id 153, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x6db7 (correct), seq 2182, ack 121076, win 7168, length 0
17:40:36.628309 IP (tos 0x0, ttl 128, id 154, offset 0, flags [none], proto TCP (6), length 314)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [P.], cksum 0xad3e (correct), seq 2182:2456, ack 121076, win 7168, length 274: HTT                                                                                                                                                              P, length: 274
        GET /global/GW1.0/01.12.031/bin/10032198-2.2-TRADFRI-gateway-1.12.31.p.elf.sig.ota.signed HTTP/1.0
        User-Agent: HertzClient/1.0 (GW (1).(8).(25); Id ae5ff982-b2a5-431a-a307-88d4d284744b)
        Host: fw.ota.homesmart.ikea.net
        Range: bytes=99976-116359
        Connection: keep-alive

17:40:36.633644 IP (tos 0x0, ttl 247, id 29620, offset 0, flags [none], proto TCP (6), length 40)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x877f (correct), seq 121076, ack 2456, win 294, length 0
17:40:36.992038 IP (tos 0x0, ttl 247, id 29628, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x98fd (correct), seq 121076:122526, ack 2456, win 294, length 1450: HT                                                                                                                                                              TP, length: 1450
        HTTP/1.1 206 Partial Content
        Content-Type: application/octet-stream
        Content-Length: 16384
        Connection: keep-alive
        x-amz-id-2: z8UHmX5DhLSMUklEbnGKSrTxUrCup9adtoQAGBh6vWBZOdIm/PBjzD1XY7nGlm+IMPL4P96pbcs=
        x-amz-request-id: D32529443F17BFEE
        x-amz-replication-status: COMPLETED
        Last-Modified: Tue, 24 Nov 2020 11:58:35 GMT
        x-amz-version-id: Q7SCltPeHFFpYmqCkNIdy.Hws_ZUJEhk
        Accept-Ranges: bytes
        Server: AmazonS3
        Date: Mon, 14 Dec 2020 14:40:00 GMT
        ETag: "6504c28dfcdebd0a5dd533ef250f1dfc"
        Content-Range: bytes 99976-116359/829224
        X-Cache: Hit from cloudfront
        Via: 1.1 d143bdfb7cce4cf7ec0bcf9ec13e5915.cloudfront.net (CloudFront)
        X-Amz-Cf-Pop: AMS1-C1
        X-Amz-Cf-Id: TxWi3oTefpz7KhMCLu9fnj5cNg5FPdIbMwhzgL4jjvre84XGxzLz3w==

17:40:36.992256 IP (tos 0x0, ttl 247, id 29629, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0xfa77 (correct), seq 122526:123976, ack 2456, win 294, length 1450: H                                                                                                                                                              TTP
17:40:36.992318 IP (tos 0x0, ttl 128, id 155, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x66fb (correct), seq 2456, ack 122526, win 7168, length 0
17:40:36.993017 IP (tos 0x0, ttl 247, id 29630, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x92c5 (correct), seq 123976:125426, ack 2456, win 294, length 1450: HT                                                                                                                                                              TP
17:40:36.993203 IP (tos 0x0, ttl 247, id 29631, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0x668b (correct), seq 125426:126876, ack 2456, win 294, length 1450: H                                                                                                                                                              TTP
17:40:36.993260 IP (tos 0x0, ttl 128, id 156, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x5ba7 (correct), seq 2456, ack 125426, win 7168, length 0
17:40:36.997635 IP (tos 0x0, ttl 247, id 29632, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x5c40 (correct), seq 126876:128326, ack 2456, win 294, length 1450: HT                                                                                                                                                              TP
17:40:37.003207 IP (tos 0x0, ttl 247, id 29637, offset 0, flags [none], proto TCP (6), length 122)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0xbf86 (correct), seq 132594:132676, ack 2456, win 294, length 82: HTT                                                                                                                                                              P
17:40:37.003387 IP (tos 0x0, ttl 247, id 29638, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0xe5e5 (correct), seq 132676:134126, ack 2456, win 294, length 1450: HT                                                                                                                                                              TP
17:40:37.797112 IP (tos 0x0, ttl 128, id 163, offset 0, flags [none], proto TCP (6), length 315)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [P.], cksum 0x267a (correct), seq 2456:2731, ack 138196, win 7168, length 275: HTT                                                                                                                                                              P, length: 275
        GET /global/GW1.0/01.12.031/bin/10032198-2.2-TRADFRI-gateway-1.12.31.p.elf.sig.ota.signed HTTP/1.0
        User-Agent: HertzClient/1.0 (GW (1).(8).(25); Id ae5ff982-b2a5-431a-a307-88d4d284744b)
        Host: fw.ota.homesmart.ikea.net
        Range: bytes=116360-132743
        Connection: keep-alive

17:40:37.802489 IP (tos 0x0, ttl 247, id 31625, offset 0, flags [none], proto TCP (6), length 40)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x4388 (correct), seq 138196, ack 2731, win 298, length 0
17:40:38.318406 IP (tos 0x0, ttl 247, id 31636, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x7e51 (correct), seq 138196:139646, ack 2731, win 298, length 1450: HT                                                                                                                                                              TP, length: 1450
        HTTP/1.1 206 Partial Content
        Content-Type: application/octet-stream
        Content-Length: 16384
        Connection: keep-alive
        x-amz-id-2: z8UHmX5DhLSMUklEbnGKSrTxUrCup9adtoQAGBh6vWBZOdIm/PBjzD1XY7nGlm+IMPL4P96pbcs=
        x-amz-request-id: D32529443F17BFEE
        x-amz-replication-status: COMPLETED
        Last-Modified: Tue, 24 Nov 2020 11:58:35 GMT
        x-amz-version-id: Q7SCltPeHFFpYmqCkNIdy.Hws_ZUJEhk
        Accept-Ranges: bytes
        Server: AmazonS3
        Date: Mon, 14 Dec 2020 14:40:00 GMT
        ETag: "6504c28dfcdebd0a5dd533ef250f1dfc"
        Content-Range: bytes 116360-132743/829224
        X-Cache: Hit from cloudfront
        Via: 1.1 d143bdfb7cce4cf7ec0bcf9ec13e5915.cloudfront.net (CloudFront)
        X-Amz-Cf-Pop: AMS1-C1
        X-Amz-Cf-Id: 00szWReTQQp4yZcDNFsNBqFGOq5Qf_ytgzfzDE4AiKO39G6UmtsZ3g==

17:40:38.318621 IP (tos 0x0, ttl 247, id 31637, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0x472d (correct), seq 139646:141096, ack 2731, win 298, length 1450: H                                                                                                                                                              TTP
17:40:38.318897 IP (tos 0x0, ttl 128, id 164, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x2308 (correct), seq 2731, ack 141096, win 5718, length 0
17:40:38.319243 IP (tos 0x0, ttl 247, id 31638, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0xe789 (correct), seq 141096:142546, ack 2731, win 298, length 1450: HT                                                                                                                                                              TP
17:40:38.319434 IP (tos 0x0, ttl 247, id 31639, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0x2da8 (correct), seq 142546:143996, ack 2731, win 298, length 1450: H                                                                                                                                                              TTP
17:40:38.319701 IP (tos 0x0, ttl 128, id 165, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x120a (correct), seq 2731, ack 143996, win 7168, length 0
17:40:38.319919 IP (tos 0x0, ttl 128, id 166, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0x120a (correct), seq 2731, ack 143996, win 7168, length 0
17:40:38.529253 IP (tos 0x0, ttl 128, id 171, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0xe5d0 (correct), seq 2731, ack 155317, win 7168, length 0
17:40:39.124982 IP (tos 0x0, ttl 128, id 172, offset 0, flags [none], proto TCP (6), length 315)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [P.], cksum 0xe976 (correct), seq 2731:3006, ack 155317, win 7168, length 275: HTT                                                                                                                                                              P, length: 275
        GET /global/GW1.0/01.12.031/bin/10032198-2.2-TRADFRI-gateway-1.12.31.p.elf.sig.ota.signed HTTP/1.0
        User-Agent: HertzClient/1.0 (GW (1).(8).(25); Id ae5ff982-b2a5-431a-a307-88d4d284744b)
        Host: fw.ota.homesmart.ikea.net
        Range: bytes=132744-149127
        Connection: keep-alive

17:40:39.136346 IP (tos 0x0, ttl 247, id 31692, offset 0, flags [none], proto TCP (6), length 40)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0xff8e (correct), seq 155317, ack 3006, win 303, length 0
17:40:39.489449 IP (tos 0x0, ttl 247, id 31727, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0x68c0 (correct), seq 155317:156767, ack 3006, win 303, length 1450: HT                                                                                                                                                              TP, length: 1450
        HTTP/1.1 206 Partial Content
        Content-Type: application/octet-stream
        Content-Length: 16384
        Connection: keep-alive
        x-amz-id-2: z8UHmX5DhLSMUklEbnGKSrTxUrCup9adtoQAGBh6vWBZOdIm/PBjzD1XY7nGlm+IMPL4P96pbcs=
        x-amz-request-id: D32529443F17BFEE
        x-amz-replication-status: COMPLETED
        Last-Modified: Tue, 24 Nov 2020 11:58:35 GMT
        x-amz-version-id: Q7SCltPeHFFpYmqCkNIdy.Hws_ZUJEhk
        Accept-Ranges: bytes
        Server: AmazonS3
        Date: Mon, 14 Dec 2020 14:40:00 GMT
        ETag: "6504c28dfcdebd0a5dd533ef250f1dfc"
        Content-Range: bytes 132744-149127/829224
        X-Cache: Hit from cloudfront
        Via: 1.1 d143bdfb7cce4cf7ec0bcf9ec13e5915.cloudfront.net (CloudFront)
        X-Amz-Cf-Pop: AMS1-C1
        X-Amz-Cf-Id: E1c_u8uBxLdlnqCohkkdLP0ANyU7vJsKlPfAq7aHzMs1qTDybs5dQQ==

17:40:39.489681 IP (tos 0x0, ttl 247, id 31728, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0x3c91 (correct), seq 156767:158217, ack 3006, win 303, length 1450: H                                                                                                                                                              TTP
17:40:39.489741 IP (tos 0x0, ttl 128, id 173, offset 0, flags [none], proto TCP (6), length 40)
    10.1.0.18.55475 > 65.9.73.117.80: Flags [.], cksum 0xdf13 (correct), seq 3006, ack 156767, win 7168, length 0
17:40:39.490674 IP (tos 0x0, ttl 247, id 31729, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [.], cksum 0xa71b (correct), seq 158217:159667, ack 3006, win 303, length 1450: HT                                                                                                                                                              TP
17:40:39.490840 IP (tos 0x0, ttl 247, id 31730, offset 0, flags [none], proto TCP (6), length 1490)
    65.9.73.117.80 > 10.1.0.18.55475: Flags [P.], cksum 0xa538 (correct), seq 159667:161117, ack 3006, win 303, length 1450: H                                                                                                                                                              TTP
