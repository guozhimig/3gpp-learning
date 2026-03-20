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
