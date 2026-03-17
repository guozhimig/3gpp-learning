# Searcher Measurement Database Update Ext
同频邻区测量值
到5G后，高通的log机制和4G发生了很大的变化，我们拿到的很多都是展示位Internal 或者加密的，==测量这种就需要从 RRC 消息中查看了== ^3vbyq4
```
2026 Jul 12  14:55:25.629  [67]  0xB97F  NR5G ML1 Searcher Measurement Database Update Ext
Subscription ID = 1
Misc ID         = 0
Major.Minor Version = 4. 0
System Time
   Slot Number = 0
   SubFrame Number = 2
   System Frame Number = 338
   Hyper System Frame Number = 1023
   SCS = 30KHZ
Num Layers = 1
SSB Periodicity Serv Cell = MS20
Frequency Offset = 1.254 PPM
Timing Offset = 2
Component Carrier List[0]
   Raster ARFCN = 633984
   CC_ID = 0
   Num Cells = 5
   Serving Cell PCI = 127
   Serving Cell Index = 0
   Serving SSB = 4
   ServingRSRP Rx23[0]
      ServingRSRP_Rx23 = NA
   ServingRSRP Rx23[1]
      ServingRSRP_Rx23 = NA
   Serving RX Beam = { NA,  }
   Serving RFIC ID = NA
   ServingSubarrayId = { NA,  }
   Cells
      ---------------------------------------------------------------------------------------------------------------------------------
      |   |      |      |     |            |            |Detected Beams                                                               |
      |   |      |      |     |            |            |     |                   |NR2NR       |NR2NR       |L2NR        |L2NR        |
      |   |      |      |     |            |            |     |RX Beam Info       |Filtered Tx |Filtered Tx |Filtered Tx |Filtered Tx |
      |   |      |      |Num  |Cell Quality|Cell Quality|SSB  |Rx Beam |Inst RSRP |Beam RSRP L3|Beam RSRQ L3|Beam RSRP L3|Beam RSRQ L3|
      |#  |PCI   |SFN   |Beams|RSRP (dBm)  |RSRQ (dBm)  |Index|Id      |(dBm)     |(dBm)       |(dBm)       |(dBm)       |(dBm)       |
      ---------------------------------------------------------------------------------------------------------------------------------
      |  0|   127|   338|    1|      -62.18|      -10.59|    4|       0|    -61.75|      -61.62|      -10.49|          NA|          NA|
      |   |      |      |     |            |            |     |       0|    -66.20|            |            |            |            |
      |  1|   128|   220|    1|      -78.63|      -15.41|    1|       0|    -77.70|      -77.69|      -15.28|          NA|          NA|
      |   |      |      |     |            |            |     |       0|    -82.55|            |            |            |            |
      |  2|   748|   216|    1|      -79.46|      -16.14|    4|       0|   -156.00|     -113.06|      -31.73|          NA|          NA|
      |   |      |      |     |            |            |     |       0|    -78.21|            |            |            |            |
      |  3|   749|   216|    1|      -78.43|      -17.38|    2|       0|    -79.09|      -78.43|      -17.38|          NA|          NA|
      |   |      |      |     |            |            |     |       0|    -80.95|            |            |            |            |
      |  4|   126|   322|    1|      -82.07|      -16.59|    1|       0|   -156.00|      -82.07|      -16.59|          NA|          NA|
      |   |      |      |     |            |            |     |       0|    -82.59|            |            |            |            |
```