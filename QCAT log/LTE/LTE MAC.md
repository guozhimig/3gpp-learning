# LTE MAC Rach Trigger

```

2026 Jul  9  15:19:52.831  [9A]  0xB061  LTE MAC Rach Trigger
Subscription ID = 1
Version = 1
Number of SubPackets = 2
SubPacket ID = 3
SubPacket - ( RACH Config Subpacket )
   Version = 9
   SubPacket Size = 28
   RACH Config V9
      Sub Id = 0
      Num Active Cell = 1
      Cell Rach Info[0]
         CC Id = 0
         Preamble initial power = -100 dB
         Power ramping step = 2 dB
         RA index1 = 48
         RA index2 = 52
         Preamble trans max = 8
         Contention resolution timer = 64 ms
         Message size Group_A = 7
         Power offset Group_B = -8 dB
         Delta preamble Msg3 = 0
         PRACH config = 3
         CS zone length = 8
         Root seq index = 220
         PRACH Freq Offset = 90
         High speed flag = 0
         Max retx Msg3 = 3
         RA rsp win size = 10 ms
SubPacket ID = 5
SubPacket - ( RACH Reason Subpacket )
   Version = 5
   Subpacket Size = 20 bytes
   RACH Reason V5
      Sub Id = 0
      CC Id = 0
      Rach reason = CONNECTION_REQ
      Maching ID = 0x5A, 0xEF, 0x71, 0xCF, 0xA0, 0x56
      RACH Contention = Contention Based RACH procedure
      Preamble = 59
      Preamble RA mask = 0xFF
      Msg3 size = 6 bytes
      Radio condn = 97 dB
      CRNTI = 0xCC47
```

# LTE MAC DL RAR Transport Block

```

2026 Jul  9  15:19:52.878  [CD]  0xB06E  LTE MAC DL RAR Transport Block
Subscription ID = 1
Version = 49
Number of SubPackets = 1
SubPacket ID = 20
SubPacket - (DL Transport Block Subpacket)
   Version = 1
   Subpacket Size = 44
   -----------------------------------------------------------------------------------------------------------------------------------------
   |    |      |   |          |    |       |   |                        |   |     |Absolute|    |      |      |     |   |     |   |        |
   |Cell|      |   |          |HARQ|DL TBS |LOG|                        |BI |Rapid|TA Val  |Hop |RB    |Coding|TBS  |TPC|UL   |CQI|        |
   |Id  |Sub-FN|SFN|RNTI Type |Id  |(bytes)|LEN|RAR TB                  |Val|Val  |(16xTs) |Flag|Assign|Scheme|Index|dB |Delay|Req|T-C-RNTI|
   -----------------------------------------------------------------------------------------------------------------------------------------
   |  96|     7|1015|   RA_RNTI|   2|     11| 11| 81 60 00 42 60 20 29 E1|  1|     |       4|   0|   304|  QPSK|    1| -6|    0|  0|  0x29E1|
   |    |      |   |          |    |       |   | 87 06 80               |   |   32|        |    |      |      |     |   |     |   |        |

```

# LTE MAC Rach Attempt

```

2026 Jul  9  15:19:52.887  [34]  0xB062  LTE MAC Rach Attempt
Subscription ID = 1
Version = 1
Number of SubPackets = 1
SubPacket ID = 6
SubPacket - ( RACH Attempt Subpacket )
   Version = 50
   Subpacket Size = 56 bytes
   RACH Attempt V50 {
      Sub Id = 0
      CC Id = 0
      Retx counter = 1
      Rach result = Success
      Contention procedure = Contention Based RACH procedure
      Msg1 - RACH Access Preamble[0]
         Preamble Index = 32
         Preamble index mask = Invalid
         Preamble power offset = -100 dB
         Pcmaxc = 22
         Group Chosen = Group A
      Msg2 - Random Access Response
         Backoff Value = 10 ms
         Result = True
         TCRNTI = 10721
         TA value = 4 
      Msg3
         Grant Raw = 0x026020
         Grant = 18 bytes
         Harq ID = 3
         MAC PDU = 0x20, 0x06, 0x1F, 0x5A, 0xEF, 0x71, 0xCF, 0xA0, 0x56, 0x00
      Earfcn = 19750
      P Max = 255
      SCell ID = 0
      Max Serv RSRP Present = FALSE
   }
```

# LTE MAC DL Transport Block

```

2026 Jul  9  15:19:52.887  [34]  0xB063  LTE MAC DL Transport Block
Subscription ID = 1
Version = 50
TB Log Buff
   Config Info
      Num Tb = 1
      Reason = 0
   TB Info[0]
      TB Common Info[0]
         -----------------------------------------------------------------------------------------
         |   |           |           |     |        |       |               |  |    |Num|        |
         |   |           |Num Pad    |     |        |Reparse|               |CC|HARQ|MAC|MAC Hdr |
         |#  |TB Size    |Bytes      |Frame|SubFrame|Flag   |RNTI Type      |ID|ID  |Sdu|Len     |
         -----------------------------------------------------------------------------------------
         |  0|         32|          0| 1016|       9|      1|       T_C_RNTI| 0|   2|  2|       3|

      MAC Sdu Info[0]
         MAC Sdu Info Table[0]
            --------------------------------------------------------------------------------------------------------------
            |   |                                  |SDU CE Info                                          |               |
            |   |                                  |RLC PDCP Info                                |       |               |
            |   |MAC Common Info                   |       |  | |  | |  |   |       |Num |       |       |Dynamic Log    |
            |   |Is |                      |       |       |  | |  | |  |   |       |PDCP|Num    |Mac CE |Info           |
            |#  |MCE|LCID                  |Sdu Len|SN     |DC|P|RF|E|FI|LSF|SO     |Grp |NLOs   |Payload|Li Num|Li Len  |
            --------------------------------------------------------------------------------------------------------------
            |  0|  1|                    28|      6|       |  | |  | |  |   |       |    |       |     90|      |        |
            |   |   |                      |       |       |  | |  | |  |   |       |    |       |    239|      |        |
            |   |   |                      |       |       |  | |  | |  |   |       |    |       |    113|      |        |
            |   |   |                      |       |       |  | |  | |  |   |       |    |       |    207|      |        |
            |   |   |                      |       |       |  | |  | |  |   |       |    |       |    160|      |        |
            |   |   |                      |       |       |  | |  | |  |   |       |    |       |     86|      |        |

      MAC Sdu Info[1]
         MAC Sdu Info Table[0]
            --------------------------------------------------------------------------------------------------------------
            |   |                                  |SDU CE Info                                          |               |
            |   |                                  |RLC PDCP Info                                |       |               |
            |   |MAC Common Info                   |       |  | |  | |  |   |       |Num |       |       |Dynamic Log    |
            |   |Is |                      |       |       |  | |  | |  |   |       |PDCP|Num    |Mac CE |Info           |
            |#  |MCE|LCID                  |Sdu Len|SN     |DC|P|RF|E|FI|LSF|SO     |Grp |NLOs   |Payload|Li Num|Li Len  |
            --------------------------------------------------------------------------------------------------------------
            |  0|  0|                     0|     23|      0| 1|0| 0|1| 0|  0|      0|   0|      0|       |      |        |

```
# LTE LL1 PDSCH Decoding Results
炳哥个plog解析下行调度就是用的这个trace
```
2026 Nov 19  10:56:11.354  [67]  0xB132  LTE LL1 PDSCH Decoding Results
Subscription ID = 1
Version = 167
Length = 160
Drop Cnt = 0
Num Records = 1
Common Static Config
   Context = LTE
   Variant Id = 0
   CxN Index = 0
   Cell Id = 436
   EARFCN = 1650
   Carrier Index = 0
   Variant Carrier Index = 0
   System BW = 20
   NIR = 228384
   Num HARQ = 9
   UE Category = 13
   TX Mode = TM2_TD_RANK1
   Num eNb Tx Ant = 2
   Four_Layer_Capability = false
TB Info Record[0]
   TB Top
      -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
      |     |     |     |    |       |      |    |    |     |    |      |         |        |         |           |         |    |    |     |    |Harq|     |   |   |     |      |      |      |
      |     |     |MVC  |    |       |      |    |    |     |    |      |         |        |         |           |         |    |IO  |     |Harq|IO  |Num  |   |   |     |      |      |      |
      |     |     |Clock|    |       |Bypass|    |Num |Start|QREN|RX01  |CB Bundle|TB DMA  |         |           |         |IO  |ST  |Num  |IO  |ST  |Harq |RP |SF |RB   |SC    |TB Ext|CB    |
      |Frame|SubFN|(MHz)|Rank|LLR BW |Decode|ITER|RX  |CB ID|BMSK|poolID|Size     |Budget  |Onld Size|Offld Size |L2 Mode  |Fail|Fail|IOVec|Fail|Fail|Iovec|Idx|Gap|Start|Index |Enable|Enable|
      -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
      |  752|    5|  288|  R2|     6B|     0|   1| 2RX|    0|   1|     0|        1|    3593|        0|         20| NO ALLOC|   0|   0|    1|   0|   0|    1|  0|  0|    0|     0|  TRUE|  TRUE|

   TB Config
      ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
      |          |    |      |     |      |   |      |        |     |    |        |               |         |      |Num     |  |      |        |        |Force  |      |Alt|Hi  |    |Excess  |      |Max|        |     |    |
      |          |HARQ|TB    |CW   |      |Num|      |        |     |Num |NCB     |               |         |      |Channel |  |CB    |        |DMA TO  |HARQ   |Bypass|MCS|MGMT|Max |HI Init |Hi    |HI |TX      |NDI  |Code|
      |RNTI      |ID  |Index |Index|Num CB|Lay|MCS   |MOD     |ReTx |ReTx|Prime   |Discard Mode   |QED Mode |Num RB|Bits    |RV|Size  |TB Size |Dur     |Offload|HARQ  |En |En  |Iter|State   |Base  |Low|Scheme  |Value|Rate|
      ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
      |        SI|   0|     0|    0|     1| 2L|     8|    QPSK|  1st|   0|     852|     NO_DISCARD|   NO_QED|    10|    2880| 0|    35|      32|2.1e+002|   TRUE| FALSE|  0|   0|17HI|       0|     0|  0|     TXD|    0|0.0972|

   TB
      -----------------------------------------------------------------------------------------------------------------------------------------------------------------------
      |TB Onload                                         |TB Offload                                         |                                                              |
      |Excess    |          |            |CB Timeout     |Excess    |          |            |CB Timeout      |TB Decode                                                     |
      |Time      |TB Pass HD|TB Pass HARQ|Status         |Time      |TB Pass HD|TB Pass HARQ|Status          |CB CRC Pass Bmsk         |Excess HI State |TB CRC     |TB Pass|
      -----------------------------------------------------------------------------------------------------------------------------------------------------------------------
      |        25|      0xFF|        0xFF|0x0000000000000000|        25|      0xFF|        0xFF|0x0000000000000000|       0x0000000000000001|               0|   0x000000|      1|

   TB Log Extend
      -------------------------------------------------------------------------------------------------------------------------------------------------------------
      |TB Ext 0   |TB Ext 1   |TB Ext 2   |TB Ext 3   |TB Ext 4   |TB Ext 5   |TB Ext 6   |TB Ext 7   |TB Ext 8   |TB Ext 9   |TB Ext 10  |TB Ext 11  |TB Ext 12  |
      -------------------------------------------------------------------------------------------------------------------------------------------------------------
      | 0x00220D83| 0x02089009| 0x000005A0| 0x008005A0| 0xC435B480| 0x40100000| 0x00000000| 0x00000000| 0x00000000| 0x00000000| 0x0004393C| 0x00000000| 0x00000000|

   CB
      --------------------------------------------------------------------------------------------------------------------------------------------------------------
      |   |                                      |                                          |CB Decode                                                             |
      |   |CB Onload                             |CB Offload                                |             |  |       |   |      |  |    |       |       |Skip  |DHB|
      |#  |On Dur|On Extract|On Time Remain|ON TO|Off Dur|Off Extract|Off Time Remain|Off TO|Energy Metric|ET|Min LLR|CRC|Num HI|HD|HARQ|CB Disc|CB Pass|Decode|IDX|
      --------------------------------------------------------------------------------------------------------------------------------------------------------------
      |  0|     0|         0|            25|    0|      0|          0|             25|     0|         8680| 1|    181|  1|   1HI| 1|   1|      0|      1|     0|  4|
```
# LTE MAC UL Transport Block

```

2026 Jul  9  15:19:52.917  [34]  0xB064  LTE MAC UL Transport Block
Subscription ID = 1
Version = 1
Number of SubPackets = 1
SubPacket ID = 8
SubPacket - ( UL Transport Block Subpacket )
   Version = 6
   Subpacket Size = 276
   Uplink Transport Block V6
      Number of samples = 16
      ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
      |Cell|       |          |      |     |Grant  |RLC  |Padding|                 |               |HDR  |                        |          |     |BSR  |BSR  |BSR  |BSR  |       |BSR LCG 0|BSR LCG 1|BSR LCG 2|BSR LCG 3|       |PH    |Pcmax_c|PH    |Pcmax_c|
      |Id  |HARQ ID|RNTI Type |Sub-FN|SFN  |(bytes)|PDUs |(bytes)|BSR event        |BSR trig       |LEN  |Mac Hdr + CE            |LC ID     |LEN  |LCG 0|LCG 1|LCG 2|LCG 3|PHR Ind|(bytes)  |(bytes)  |(bytes)  |(bytes)  |Pcmax_c|SCell1|SCell1 |SCell2|SCell2 |
      ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
      |   0|      0|    C-RNTI|     6| 1017|     19|    0|     12|             None|      Pad L-BSR|    7| 3E 3A 1F 00 00 00 25   |     L-BSR|    3|    0|    0|    0|    0|       |        0|        0|        0|        0|       |      |       |      |       |
      |    |       |          |      |     |       |     |       |                 |               |     |                        |       PHR|    1|     |     |     |     |     37|         |         |         |         |       |      |       |      |       |
      |    |       |          |      |     |       |     |       |                 |               |     |                        |   Padding|   -1|     |     |     |     |       |         |         |         |         |       |      |       |      |       |
      |   0|      1|    C-RNTI|     7| 1017|     19|    0|     12|             None|      Pad L-BSR|    7| 3E 3A 1F 00 00 00 22   |     L-BSR|    3|    0|    0|    0|    0|       |        0|        0|        0|        0|       |      |       |      |       |
      |    |       |          |      |     |       |     |       |                 |               |     |                        |       PHR|    1|     |     |     |     |     34|         |         |         |         |       |      |       |      |       |
      |    |       |          |      |     |       |     |       |                 |               |     |                        |   Padding|   -1|     |     |     |     |       |         |         |         |         |       |      |       |      |       |
      |   0|      2|    C-RNTI|     8| 1017|     19|    0|     14|             None|      Pad L-BSR|    5| 3E 1F 00 00 00         |     L-BSR|    3|    0|    0|    0|    0|       |        0|        0|        0|        0|       |      |       |      |       |
      |    |       |          |      |     |       |     |       |                 |               |     |                        |   Padding|   -1|     |     |     |     |       |         |         |         |         |       |      |       |      |       |
      |   0|      3|    C-RNTI|     9| 1017|     19|    1|      0|             None|         No BSR|    1| 01                     |         1|   -1|     |     |     |     |       |         |         |         |         |       |      |       |      |       |
      |   0|      4|    C-RNTI|     0| 1018|     19|    1|      0|High Data Arrival|          S-BSR|    3| 3D 01 10               |     S-BSR|    1|   16|     |     |     |       |      107|         |         |         |       |      |       |      |       |
      |    |       |          |      |     |       |     |       |                 |               |     |                        |         1|   -1|     |     |     |     |       |         |         |         |         |       |      |       |      |       |
      |   0|      5|    C-RNTI|     1| 1018|     19|    1|      0|             None|         No BSR|    1| 01                     |         1|   -1|     |     |     |     |       |         |         |         |         |       |      |       |      |       |
      |   0|      6|    C-RNTI|     2| 1018|     19|    1|      0|             None|         No BSR|    1| 01                     |         1|   -1|     |     |     |     |       |         |         |         |         |       |      |       |      |       |
      |   0|      7|    C-RNTI|     3| 1018|     19|    1|      0|             None|         No BSR|    1| 01                     |         1|   -1|     |     |     |     |       |         |         |         |         |       |      |       |      |       |
      |   0|      0|    C-RNTI|     4| 1018|     19|    1|      0|             None|         No BSR|    1| 01                     |         1|   -1|     |     |     |     |       |         |         |         |         |       |      |       |      |       |
      |   0|      1|    C-RNTI|     5| 1018|     19|    1|      0|         Periodic|          S-BSR|    3| 3D 01 06               |     S-BSR|    1|    6|     |     |     |       |       22|         |         |         |       |      |       |      |       |
      |    |       |          |      |     |       |     |       |                 |               |     |                        |         1|   -1|     |     |     |     |       |         |         |         |         |       |      |       |      |       |
      |   0|      2|    C-RNTI|     6| 1018|     57|    1|     27|             None|      Pad L-BSR|    7| 3E 21 17 1F 00 00 00   |     L-BSR|    3|    0|    0|    0|    0|       |        0|        0|        0|        0|       |      |       |      |       |
      |    |       |          |      |     |       |     |       |                 |               |     |                        |         1|   23|     |     |     |     |       |         |         |         |         |       |      |       |      |       |
      |    |       |          |      |     |       |     |       |                 |               |     |                        |   Padding|   -1|     |     |     |     |       |         |         |         |         |       |      |       |      |       |
      |   0|      3|    C-RNTI|     7| 1018|    129|    0|    124|             None|      Pad L-BSR|    5| 3E 1F 00 00 00         |     L-BSR|    3|    0|    0|    0|    0|       |        0|        0|        0|        0|       |      |       |      |       |
      |    |       |          |      |     |       |     |       |                 |               |     |                        |   Padding|   -1|     |     |     |     |       |         |         |         |         |       |      |       |      |       |
      |   0|      5|    C-RNTI|     9| 1018|     41|    0|     36|             None|      Pad L-BSR|    5| 3E 1F 00 00 00         |     L-BSR|    3|    0|    0|    0|    0|       |        0|        0|        0|        0|       |      |       |      |       |
      |    |       |          |      |     |       |     |       |                 |               |     |                        |   Padding|   -1|     |     |     |     |       |         |         |         |         |       |      |       |      |       |
      |   0|      7|    C-RNTI|     1| 1019|     41|    0|     36|             None|      Pad L-BSR|    5| 3E 1F 00 00 00         |     L-BSR|    3|    0|    0|    0|    0|       |        0|        0|        0|        0|       |      |       |      |       |
      |    |       |          |      |     |       |     |       |                 |               |     |                        |   Padding|   -1|     |     |     |     |       |         |         |         |         |       |      |       |      |       |
      |   0|      0|    C-RNTI|     2| 1019|     41|    0|     36|             None|      Pad L-BSR|    5| 3E 1F 00 00 00         |     L-BSR|    3|    0|    0|    0|    0|       |        0|        0|        0|        0|       |      |       |      |       |
      |    |       |          |      |     |       |     |       |                 |               |     |                        |   Padding|   -1|     |     |     |     |       |         |         |         |         |       |      |       |      |       |
      |   0|      6|    C-RNTI|     8| 1019|    113|    2|      0|High Data Arrival|          S-BSR|    5| 3D 21 02 01 03         |     S-BSR|    1|    3|     |     |     |       |       14|         |         |         |       |      |       |      |       |
      |    |       |          |      |     |       |     |       |                 |               |     |                        |         1|    2|     |     |     |     |       |         |         |         |         |       |      |       |      |       |
      |    |       |          |      |     |       |     |       |                 |               |     |                        |         1|   -1|     |     |     |     |       |         |         |         |         |       |      |       |      |       |


```