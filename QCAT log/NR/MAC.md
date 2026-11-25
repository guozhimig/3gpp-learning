# NR5G MAC PDSCH Status
查看下行调度情况，观察诸如调度的rb
```
2026 Nov 19  10:55:54.608  [CD]  0xB887  NR5G MAC PDSCH Status
Subscription ID = 1
Misc ID         = 0
Major.Minor = 4. 1
Num Records = 1
Records
   ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
   |   |                     |      |PDSCH Status Info                                                                                                                                                                                                                                                                                                  |
   |   |                     |      |       |    |      |    |         |    |       |        |        |     |        |   |   |   |  |HARQ |              |    |   |      |         |        |      |    |   |       |      |      |    |       |       |       |       |      |     |        |     |        |          |          |          |          |
   |   |                     |      |       |    |      |    |         |    |       |        |        |     |        |   |   |   |  |Or   |              |K1  |   |      |         |        |      |    |   |       |      |      |    |       |       |       |       |      |     |        |     |        |          |          |          |          |
   |   |                     |Num   |       |    |      |    |         |    |       |        |        |     |        |   |   |   |  |MBSFN|              |Or  |   |      |         |        |      |New |   |       |      |      |    |HD     |HARQ   |HD     |HARQ   |      |Is   |        |High |        |          |          |          |          |
   |   |System Time          |PDSCH |Carrier|Tech|      |Conn|         |Band|Variant|Physical|        |TB   |        |SCS|   |Num|  |Area |              |PMCH|   |Num   |Iteration|CRC     |CRC   |Tx  |   |Discard|Bypass|Bypass|Num |Onload |Onload |Offload|Offload|Did   |IOVec|        |Clock|        |Rx Antenna|Rx Antenna|Rx Antenna|Rx Antenna|
   |#  |Slot|Numerology|Frame|Status|ID     |Id  |Opcode|ID  |Bandwidth|Type|Id     |Cell ID |EARFCN  |Index|TB Size |MU |MCS|Rbs|RV|Id   |RNTI Type     |ID  |TCI|Layers|Index    |State   |Status|Flag|NDI|Mode   |Decode|HARQ  |ReTx|Timeout|Timeout|Timeout|Timeout|Recomb|Valid|Mod Type|Mode |Num RX  |Mapping 0 |Mapping 1 |Mapping 2 |Mapping 3 |
   ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
   |  0|  12|     30KHZ|  101|     1|      0|   1|     0|   0|    20MHz|   0|      0|      37|  633984|    0|       9|  1|  0|  3|NA|   NA|        P RNTI|  NA|  0|     1|        0|    PASS|  PASS|   1| NA|      0|     0|     1|   0|      0|      0|      0|      0|     0| TRUE|    QPSK|    0|2X2_MIMO|         0|         0|         0|         0|

```
# UL Physical Channel Schedule Report

# UL Physical Channel Power Control
```

2026 Jul 12  11:19:35.493  [CD]  0xB884  NR5G MAC UL Physical Channel Power Control
Subscription ID = 1
Misc ID         = 0
Major.Minor Version = 4. 0
Num Records = 1
Records
   -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
   |   |      |      |      |        |          |Carriers                                                                                                                                                                                                                |
   |   |      |      |      |        |          |        |Power Params                                                                                                                                                                                                   |
   |   |      |      |      |        |          |        |       |       |        |        |          |    |        |         |    |    |     |      |    |        |        |       |PRACH         |                |PUSCH                    |PUCCH                     |
   |   |      |      |      |        |          |        |       |       |        |        |          |    |        |         |    |    |     |      |    |        |        |       |       |PRACH |SRS             |     |     |Num   |      |     |      |Num   |      |
   |   |      |      |System|        |Timing    |        |       |       |Transmit|        |TPC       |PHR |        |Antenna  |TX  |Use |Use  |      |    |Spatial |Spatial |Minimum|       |Target|         |Rampup|Delta|     |Symbol|Rampup|Delta|      |Symbol|Rampup|
   |   |Slot  |      |Frame |Num     |Reference |Num     |Carrier|Channel|Power   |Pathloss|Adjustment|MTPL|Channel |Switch   |Port|Pmin|PRACH|Start |Num |Relation|Relation|Power  |RACH   |Power |SRS      |Power |TF   |RAR  |First |Power |TF   |PUCCH |First |Power |
   |#  |Number|SCS   |Number|Carriers|Number    |Channels|ID     |Type   |(dB)    |(dB)    |(dB)      |(dB)|Priority|Indicator|Mask|Beam|Beam |Symbol|Hops|Type    |Info    |(dB)   |Attempt|(dB)  |Bandwidth|(dB)  |(dB) |PUSCH|Hop   |(dB)  |(dB) |Format|Hop   |(dB)  |
   -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
   |  0|     9| 30KHZ|   552|       1|     11049|       1|      0|  PUCCH|    25.0|   121.0|       1.0|22.0|       1|        0|   1|   0|    0|     0|   1|       0|      15|  -47.0|       |      |         |      |     |     |      |      |  0.0|     1|     7|   0.0|


```
# UCI Payload Information
```
Subscription ID = 1
Misc ID         = 0
Major.Minor = 4. 0
Num Records = 1
Records
   ---------------------------------------------------------------------------------------------------------------------------------------
   |   |                      |        |Channel Info                                                                                     |
   |   |                      |        |          |       |      |       |    |    |Num |Num |          |          |          |          |
   |   |                      |        |          |       |      |       |Num |Num |CSF |CSF |          |          |          |          |
   |   |System Time           |Num     |          |Carrier|Start |Num    |HARQ|SR  |P1  |P2  |HARQ      |          |CSI P1    |CSI P2    |
   |#  |Slot|Numerology|Frame |Channels|Channel   |ID     |Symbol|Symbols|Bits|Bits|Bits|Bits|Payload   |SR Payload|Payload   |Payload   |
   ---------------------------------------------------------------------------------------------------------------------------------------
   |  0|  14|     30kHz|   551|       1|PUCCH_FMT1|      0|     0|     14|   2|   0|   0|   0|         3|          |          |          |
```