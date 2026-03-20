# LTE ML1 Serving Cell Meas Response

服务小区测量
```
2026 Jun 26  14:06:32.415  [00]  0xB193  LTE ML1 Serving Cell Meas Response
Subscription ID = 1
Version = 1
Number of SubPackets = 1
SubPacket ID = 25
Serving Cell Measurement Result
   Version = 56
   SubPacket Size = 176 bytes
   E-ARFCN = 1506
   Num of Cell = 1
   Cells[0]
      Valid Rx = RX0_RX1
      Logical To Physical Rx Map = { 1, 0, NA, NA }
      Physical Cell ID = 367
      Serving Cell Index = PCell
      FW Serving Cell Index = 0
      Is Serving Cell = 1
      Current SFN = 802
      Current Subframe Number = 7
      Is Restricted = false
      Cell Timing[0] = 5728
      Cell Timing[1] = 5728
      Cell Timing SFN[0] = 802
      Cell Timing SFN[1] = 802
      Inst RSRP Rx[0] = -84.19 dBm
      Inst RSRP Rx[1] = -76.88 dBm
      Inst RSRP Rx[2] = NA
      Pathloss RSRP Rx[2] = NA
      Pathloss RSRP Rx[3] = NA
      Inst RSRP Rx[3] = NA
      Inst Measured RSRP = -76.88 dBm
      Filtered RSRP = -77.81 dBm
      Inst RSRQ Rx[0] = -16.88 dB
      Inst RSRQ Rx[1] = -16.19 dB
      Inst RSRQ Rx[2] = NA
      Inst RSRQ Rx[3] = NA
      Inst RSRQ = -16.19 dB
      Filtered RSRQ = -13.00 dB
      Inst RSSI Rx[0] = -50.31 dBm
      Inst RSSI Rx[1] = -43.69 dBm
      Inst RSSI Rx[2] = NA
      Inst RSSI Rx[3] = NA
      Inst RSSI = -43.69 dBm
      FTL SNR Rx[0] = 2.60 dB
      FTL SNR Rx[1] = 5.30 dB
      FTL SNR Rx[2] = NA
      FTL SNR Rx[3] = NA
      Projected Sir = 0 dB
      Post Ic Rsrq = -2e+001 dB
      CINR RX 0 = 448
      CINR RX 1 = 1223
      CINR RX 2 = NA
      CINR RX 3 = NA
```

# LTE ML1 Serving Cell Meas and Eval

```
```
# LTE ML1 Cell Measurement Results

服务小区和同频邻区测量

```
2026 Jun 26  14:06:32.493  [CD]  0xB196  LTE ML1 Cell Measurement Results
Subscription ID = 1
Version = 41
Num Cells = 3
Is 1Rx Mode = 0
Cell Measurement List
   ------------------------------------------------------------------------------
   |   |       |        |       |Inst   |Inst   |Inst   |Inst   |Inst   |Inst   |
   |   |       |        |       |RSRP   |RSRP   |RSRQ   |RSRQ   |RSSI   |RSSI   |
   |   |       |Physical|Valid  |Rx[0]  |Rx[1]  |Rx[0]  |Rx[1]  |Rx[0]  |Rx[1]  |
   |#  |E-ARFCN|Cell ID |Rx     |(dBm)  |(dBm)  |(dBm)  |(dBm)  |(dBm)  |(dBm)  |
   ------------------------------------------------------------------------------
   |  0|   1506|     367|RX0_RX1| -84.13| -76.88| -14.75| -13.63| -52.31| -46.25|
   |  1|   1506|     335|RX0_RX1| -86.25| -89.75| -22.50| -17.88| -54.69| -62.81|
   |  2|   1506|     229|RX0_RX1| -88.06| -93.75| -22.56| -23.00| -56.44| -61.75|
```

# LTE ML1 Connected Mode LTE Intra-Freq Meas Results

同频邻区的测量, 这个打印的频率比较低，感觉还不如直接看 [LTE ML1 Cell Measurement Results](#LTE%20ML1%20Cell%20Measurement%20Results)

```
2026 Jun 26  14:06:33.048  [CD]  0xB179  LTE ML1 Connected Mode LTE Intra-Freq Meas Results
Subscription ID = 1
Version = 56
Serving Cell Index = PCell
FW Serving Cell Index = PCell
E-ARFCN = 1506
Serving Physical Cell ID = 367
Sub-frame Number = 8664
Serving Filtered RSRP = -76.88 dBm
Serving Filtered RSRQ = -10.88 dB
Number of Neighbor Cells = 2
Number of Detected Cells = 0
Neighbor Cells
   --------------------------------
   |   |        |Filtered|Filtered|
   |   |Physical|RSRP    |RSRQ    |
   |#  |Cell ID |(dBm)   |(dB)    |
   --------------------------------
   |  0|     335|  -84.75|  -17.31|
   |  1|     229|  -87.88|  -22.75|
```


# LTE ML1 Neighbor Cell Meas Request/Response

异频邻区的测量
```
2026 Jun 26  14:06:33.048  [CD]  0xB195  LTE ML1 Connected Neighbor Meas Request/Response
Subscription ID = 1
Version = 1
Number of SubPackets = 2
SubPacket ID = 30
Connected Neighbor Meas Request
   Version = 56
   SubPacket Size = 48 bytes
   E-ARFCN = 1506
   Num Neighbor Cells = 2
   Num Rx Ant = 2
   Serving Cell Index = PCell
   FW Serving Cell Index = 0
   Num Ms Per Cell = 1 ms
   Meas Req Act Time = 8657
   Neighbor Cells
      --------------------------------------------------------------------------
      |   |    |              |   |        |Frame     |Frame     |Total |Total |
      |   |    |              |eNb|        |Boundary  |Boundary  |Timing|Timing|
      |   |Cell|              |Tx |TTL     |Ref       |Ref       |Adj   |Adj   |
      |#  |ID  |CP Type       |Ant|Enable  |Time[0]   |Time[1]   |CIR[0]|CIR[1]|
      --------------------------------------------------------------------------
      |  0| 335|        Normal|  2|Disabled|      5737|      5737|     0|     0|
      |  1| 229|        Normal|  2|Disabled|      5801|      5801|     0|     0|

SubPacket ID = 31
Connected Neighbor Meas Response
   Version = 56
   SubPacket Size = 116 bytes
   E-ARFCN = 1506
   Num Cells = 2
   Duplexing Mode = FDD
   Serving Cell Index = PCell
   FW Serving Cell Index = 0
   Meas Resp Sfn = 8664
   Neighbor Cells
      ---------------------------------------------------------------------------------------------------
      |   |        |           |Inst   |Inst   |Inst    |Inst   |Inst   |       |Inst   |Inst   |       |
      |   |        |FTL        |RSRP   |RSRP   |Measured|RSRQ   |RSRQ   |Inst   |RSSI   |RSSI   |Inst   |
      |   |Physical|Cumulative |Rx[0]  |Rx[1]  |RSRP    |Rx[0]  |Rx[1]  |RSRQ   |Rx[0]  |Rx[1]  |RSSI   |
      |#  |Cell ID |Freq Offset|(dBm)  |(dBm)  |(dBm)   |(dBm)  |(dBm)  |(dBm)  |(dBm)  |(dBm)  |(dBm)  |
      ---------------------------------------------------------------------------------------------------
      |  0|     335|          0| -85.69| -86.25|  -85.69| -23.25| -17.19| -17.19| -53.44| -60.00| -53.44|
      |  1|     229|          0| -88.94| -92.31|  -88.94| -26.50| -23.25| -23.25| -53.44| -60.00| -53.44|
```
