# LTE RLC DL Statistics

```

2026 Jul  9  15:19:52.887  [34]  0xB087  LTE RLC DL Statistics
Subscription ID = 1
Version = 64
Num RB = 1
Reason = 0
Num FC Down Commands = 0
Num FC Up Commands = 0
Num Shutdown Issued = 0
Num RLF Issued = 142
Num FC Level1 Down Commands = 0
Num FC Level1 Up Commands = 1077
Num Scell FC Start = 0
Num Scell FC Stop = 0
Num FC RX Win = 29
Last RLF = 508322227
Num FC Level1 Inc Segs Dropped = { 0, 0, 0, 0 }
Num FC Level1 History Index = 0
Num FC Shutdown Inc Segs Dropped = 0
RB Stats
   -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
   |   |RB    |    |            |            |            |            |            |Num         |            |            |            |            |            |            |            |Num         |Num         |            |            |Num Status  |Num Status  |Num Status  |Num Status  |          |          |          |
   |   |Config|RB  |            |            |Num Status  |Num Invalid |            |Duplicate   |Num Dropped |Num Segment |Num Segment |Num Status  |Num Status  |Num Status  |Num Status  |Reassembly  |Reassembly  |Num Missed  |Num Meta    |Trigger Ack |Trigger Nack|Update Ack  |Update Nack |Num Status|Num Status|RLC Data  |
   |#  |Index |Mode|Num RLC Meta|Num Data PDU|Rxed        |PDUs        |Num ReTx PDU|PDU         |PDU         |Join        |Collapse    |Trigger     |Update      |OTA         |PDU Drop    |Expired     |Start       |UM PDU      |Overlap     |SN Only     |List        |SN Only     |List        |Ackd      |Nack Lists|Bytes     |
   -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
   |  0|    33|   1|           0|           0|           0|           0|           0|           0|           0|           0|           0|           0|           0|           0|           0|           0|           0|           0|           0|           0|           0|           0|           0|         0|         0|         0|


```

# LTE RLC DL AM Control PDU

```

2026 Jul  9  15:19:52.887  [34]  0xB083  LTE RLC DL AM Control PDU
Subscription ID = 1
Version = 48
Num Control PDU = 7
PDUs
   ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
   |   |        |      |      |       |Payload                                                                                                                                                                                              |
   |   |        |      |      |       |AM PDU                                                                                            |AM PDU SNL 16 Bits                                                                                |
   |   |Sys Time|RB    |      |Control|               |RLCDL |                  |                  |                  |                  |               |RLCDL |                  |                  |                  |                  |
   |   |Sub|    |Config|SN    |PDU    |               |CTRL :|                  |                  |                  |                  |               |CTRL :|                  |                  |                  |                  |
   |#  |FN |SFN |Index |Length|Size   |cpt            |ACK_SN|RLCDL CTRL NACK_SN|NACK_SN           |SOstart           |SOend             |cpt            |ACK_SN|RLCDL CTRL NACK_SN|NACK_SN           |SOstart           |SOend             |
   ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
   |  0|  4|  14|1     |10    |2      |     STATUS (0)|   752|                  |                  |                  |                  |               |      |                  |                  |                  |                  |
   |  1|  9|  19|1     |10    |2      |     STATUS (0)|   795|                  |                  |                  |                  |               |      |                  |                  |                  |                  |
   |  2|  4|  25|1     |10    |2      |     STATUS (0)|   838|                  |                  |                  |                  |               |      |                  |                  |                  |                  |
   |  3|  9|  30|1     |10    |2      |     STATUS (0)|   873|                  |                  |                  |                  |               |      |                  |                  |                  |                  |
   |  4|  4|  36|1     |10    |2      |     STATUS (0)|   908|                  |                  |                  |                  |               |      |                  |                  |                  |                  |
   |  5|  9|  41|1     |10    |2      |     STATUS (0)|   948|                  |                  |                  |                  |               |      |                  |                  |                  |                  |
   |  6|  4|  47|1     |10    |2      |     STATUS (0)|   969|                  |                  |                  |                  |               |      |                  |                  |                  |                  |

```


# LTE RLC DL AM All PDU

```

2026 Jul  9  15:19:52.887  [34]  0xB082  LTE RLC DL AM All PDU
Subscription ID = 1
Version = 48
Num Meta = 13
Num Rb = 1
Rlc State
   ---------------------------------------
   |Rb |    |Rlc|    |Rx Next|Rx    |Rx  |
   |Cfg|Rb  |Sn |Rx  |Status |High  |Next|
   |Idx|Mode|Len|Next|Trigger|Status|High|
   ---------------------------------------
   | 33|  AM| 10|   0|      0|     0|   0|

Meta Log
   -----------------------------------------------------------------------------------------------------------------
   |Sys Time|Rb |          |      |      |          |          | |   |    |    |     |       |          |          |
   |Sub|    |Cfg|          |Start |      |          |          | |   |Tail|Head|Inner|Payload|First Pdcp|Last Pdcp |
   |FN |SFN |Idx|Status    |Sn    |End Sn|So Start  |So End    |P|Lsf|Seg |Seg |Seg  |Len    |Sn        |Sn        |
   -----------------------------------------------------------------------------------------------------------------
   |  3|  43|  1|  PDU DATA|   669|   669|       0x0|0xFFFFFFFF|1|  0|   0|   0|    0|     84|      3970|      3971|
   |  5|  44|  1|  PDU DATA|   677|   677|       0x0|0xFFFFFFFF|1|  0|   0|   0|    0|     84|      3984|      3985|
   |  0|  45|  1|  PDU DATA|   678|   678|       0x0|0xFFFFFFFF|1|  0|   0|   0|    0|    126|      3986|      3988|
   |  3|  45|  1|  PDU DATA|   679|   679|       0x0|0xFFFFFFFF|1|  0|   0|   0|    0|     84|      3989|      3990|
   |  6|  45|  1|  PDU DATA|   681|   681|       0x0|0xFFFFFFFF|1|  0|   0|   0|    0|     42|      3993|      3993|
   |  8|  45|  1|  PDU DATA|   682|   682|       0x0|0xFFFFFFFF|1|  0|   0|   0|    0|     42|      3994|      3994|
   |  9|  45|  1|  PDU DATA|   683|   683|       0x0|0xFFFFFFFF|1|  0|   0|   0|    0|     42|      3995|      3995|
   |  3|  46|  1|  PDU DATA|   680|   680|       0x0|0xFFFFFFFF|1|  0|   0|   0|    0|     84|      3991|      3992|
   |  4|  49|  1|  PDU DATA|   684|   684|       0x0|0xFFFFFFFF|1|  0|   0|   0|    0|     42|      3996|      3996|
   |  5|  49|  1|  PDU DATA|   685|   685|       0x0|0xFFFFFFFF|1|  0|   0|   0|    0|     84|      3997|      3998|
   |  6|  49|  1|  PDU DATA|   686|   686|       0x0|0xFFFFFFFF|1|  0|   0|   0|    0|     42|      3999|      3999|
   |  8|  49|  1|  PDU DATA|   687|   687|       0x0|0xFFFFFFFF|1|  0|   0|   0|    0|     84|      4000|      4001|
   |  1|  50|  1|  PDU DATA|   689|   689|       0x0|0xFFFFFFFF|1|  0|   0|   0|    0|     84|      4005|      4006|


```